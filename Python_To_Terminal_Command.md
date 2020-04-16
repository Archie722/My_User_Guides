
How to make a Python program executable in terminal just by typing the name of the file as a command from any directory<br/>
<br/>
1. Create a folder to store the programs, eg:<br/>
<br/>
**/Users/User/bin**<br/>
<br/>
2. Enter the shebang line on the very first line of the python program.<br/>
<br/>
To find where the version of python you are running is, type in terminal:<br/>
<br/>
**which python**<br/>
<br/>
The Shebang line should look something like:<br/>
<br/>
**#!/Users/User/anaconda3/bin/python**<br/>
<br/>
3. The file itself needs to be made executable. Navigate to the folder the file is saved in. In Terminal type:<br/>
<br/>
**Chmod +x filename.py**<br/>
<br/>
4. Check that the file executes correctly by typing:<br/>
<br/>
**./filename.py**<br/>
<br/>
It should run without having to type python filename.py<br/>
<br/>
4. Now add the folder you created to the $PATH. This is where the system will look for any ‘commands’ typed into terminal.<br/>
In terminal type:<br/>
<br/>
**vi ~/.bash_profile**<br/>
<br/>
This opens bash_profile in VIM editor<br/>
<br/>
Type:<br/>
<br/>
**i**<br/>
<br/>
to insert/make changes<br/>
<br/>
insert this line to the top:<br/>
<br/>
**export PATH="/Users/User/bin:$PATH"**<br/>
<br/>
(or whatever path to the folder you created)<br/>
<br/>
5. Now when when you type the filename in from any directory in terminal it should run that file.<br/>
<br/>
Make sure you ‘SAVE AS’ the file without the .py extension, otherwise you will have to type filename.py to run the command
