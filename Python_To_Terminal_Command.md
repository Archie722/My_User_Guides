## title
How to make a Python program executable in terminal just by typing the name of the file as a command from any directory.
1. Create a folder to store the programs, eg:
**/Users/User/bin**<br/>
2. Enter the shebang line on the very first line of the python program.
To find where the version of python you are running is, type in terminal:
**which python**
The Shebang line should look something like:
**#!/Users/User/anaconda3/bin/python**
3. The file itself needs to be made executable. Navigate to the folder the file is saved in. In Terminal type:
**Chmod +x filename.py**
4. Check that the file executes correctly by typing:
**./filename.py**
It should run without having to type python filename.py
4. Now add the folder you created to the $PATH. This is where the system will look for any ‘commands’ typed into terminal.
In terminal type:
**vi ~/.bash_profile**
This opens bash_profile in VIM editor
Type:
**i**
to insert/make changes
insert this line to the top:
**export PATH="/Users/User/bin:$PATH"**
(or whatever path to the folder you created)
5. Now when when you type the filename in from any directory in terminal it should run that file.
Make sure you ‘SAVE AS’ the file without the .py extension, otherwise you will have to type filename.py to run the command
