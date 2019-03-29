# Terminal For Beginner (Mac/Linux)
For those who want to learn more about the terminal commands on Mac/Linux
___
___
___

### What is Bash
A shell is a UI that allows for interacting with computer resources.
Bash is the default command line shell on mac , linux.  Bourne Again Shell.  
Bash is a simple programming/scripting language

## Commands
`pwd,cd and ls`
___
* pwd => present working directory
* ls => list file/folders in the current directory
* ls -l => long list , shows owner group
* cd  => change directory 
* cd .. =>  move up one level
* cd / => goes to root of the pc
* cd User => goes to the Users directory
* cd ~ or cd =>  takes us to the root page

## The Basics
 ##### Cleaning up (clear and exiting)
___
* clear => clears the screen , this pushes up the screen
* cmd + k => clears the session totally 
* exit => cmd + q to exit the terminal
* echo => echoes back what we enter to it , we can also use to display path variables
   `echo $PATH`
   `echo "The current path is $PATH"` (variable interpolation)
* which => to find where commands are located
`which ls`
`which which`
* man commandName => get help about a command
   `man ls`  up or down to navigate and q to exit
or google : ls command

##### Looking or Reviewing files 
___
* cat : come from concatenate
    `cat filename`
   Good when the file is small
* less : `less filename`
   It helps us navigate up and down the file , use q to exit
  When the file to view large
* nano : can be used to modified a file , then navigate and make modification then Ctrl X to save changes and either rename if you want
## Using TextMate
mate fileName.txt
command w => to close the file
command q => to quit textmate
## Accessing file and directory with the `OPEN` command
open ~ => opens the directory 
open fileName.txt =>  the file is open with the default file editor
## Create create , move , rename and delete files
##### Create file
____
touch fileName.txt => to create a file
To update the timestamp of a file , ie an application looking for updated files will need this functionality  
Just do a touch command on the existing file it will update the timestamp of the file
touch existingFile.txt    
##### Move file
___
mv currentFileName.txt newFileName.txt => to rename a file
mv currentFileName.txt DirectoryName => to move the file to a new directory
##### Copy file
___
cp CopyContentFrom.txt CopyContentTo.txt
cp Seun.txt Seun2.txt
##### Remove file
___
rm fileName.txt
rm *-2.txt (remove any file that ends with -2.txt)
### Create and delete directories
##### Create directory
___
mkdir DirectoryName
We can `cd` into it then `cd ..` to move out of it 
##### Delete directory
___
rmdir DirectoryName 
Tree directory
___
Directory with files inside of it 
mkdir -p Seun/Books/Title
This will create 3 folder as specified
To remove these folder recursively 
rm -rf Seun => this will remove the 3 folders
### Output Redirection
echo "Hello World" >> hello.txt
This will write "Hello World" into hello.txt
To see it 
cat hello.txt

We can append more text to this file 
echo "You are welcome to my world" >> hello.txt

cat hello.txt
NOTE : that the >> will append while the > will replace the entire content of the file

echo "Welcome to my world" > hello.txt

Above will replace the content of the entire file with the text about

NOTE : > and >> is known as input/output redirection
ls -l > listing.txt => This will redirect the output of the file into the listing.txt
### Chaining commands together with Pipes |
For example we want to show the result from our ls -l and also redirect it into a file  , this is like doing 2 things at the same time

We need the `tee` command in this case also : the __tee__ utility copies standard input to standard output , making a copy in zero or more files. The output is unbuffered.
eg
`ls -l | tee listing.txt`

These are 2 commands 
ls -l : list the content of the current directory
|     : send the content of the command into another command
tee   : send the content into file





