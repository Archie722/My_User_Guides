## How to make your Python program execute as a command in Terminal
How to make a Python program executable in terminal just by typing the name of the file as a command from any directory.<br/>
1. Create a folder to store the programs, eg:<br/>
**/Users/User/bin**<br/><br/>
2. Enter the shebang line on the very first line of the python program.
To find where the version of python you are running is, type in terminal:<br/>
**which python**<br/><br/>
The Shebang line should look something like:<br/>
**#!/Users/User/anaconda3/bin/python**<br/><br/>
This tells the interpreter what language the code is written in and how to execute it.<br/><br/>
3. The file itself needs to be made executable. Navigate to the folder the file is saved in. In Terminal type:<br/>
For Example:<br/>
**cd Users/User/bin**<br/><br/>
Then we change the permissions of the file to make it executable (like a .exe file in windows)<br/>
**Chmod +x filename.py**<br/><br/>
4. Check that the file executes correctly by typing:<br/>
**./filename.py**<br/><br/>
The ./ denotes you are working in Terminal from the current directory the file is in.<br/>
It should run without having to type **python filename.py**<br/><br/>
4. Now add the **bin** folder you created to the **$PATH**. This is where the system will look for any ‘commands’ typed into terminal.<br/>
In terminal type:<br/>
**vi ~/.bash_profile**<br/><br/>
This opens bash_profile in VIM editor (or use an editor of your choice, nano is a good one - **nano ~/.bash_profile**)<br/>
The ~/. is just bavigating to the Home directory, as that is where .bash_profile is normally saved.<br/>
The '.' meens the file is hidden. If using VIM editor, type:<br/>
**i**<br/>
to insert/make changes<br/>
insert this line to the top:<br/>
**export PATH="/Users/User/bin:$PATH"**<br/><br/>
(or whatever path to the folder you created)<br/><br/>
5. Now when when you type the filename in from any directory in terminal it should run that file.<br/><br/>
**Point to Note** - Make sure you **‘SAVE AS’** the file without the .py extension, otherwise you will have to type filename.py to run the command. The shebang line is used to identify the interpreter to run the code rather than the .py.
To run your Python program in command prompt, you should be able to open Terminal, and from any directory type the filename to execute the program.
