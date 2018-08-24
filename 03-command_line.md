# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

1. _**'pwd'**_ =  Print Working Directory  
2. _**'mkdir'**_ = short for Make Directory  
3. _**'rmdir'**_ = removes directory  
4. _**'touch'**_ = creates an  empty file  
5. _**'rm'**_ = removes file from directory  
6. _**'mv'**_ = moves files from one directory to another (_Example: mv ~/Documents/lee_personal/work/test1.txt ~/Documents/lee_personal/work/test2.txt_)  
7. _**'ls -a**_ = List all the hidden files too. Any files starting with a dot in front of it is a hidden file
8. _**'cp'**_ = stands for copy.(_Example: cp ~/Documents/lee_personal/work/temp/test1.txt ~/Documents/lee_personal/work/test2.txt_)  
9. _**'wc'**_ = Stands for word count  
    - _'wc -l'_ = will give the number of lines  
    - _'wc -w'_ = will give the number of words  
    - _'wc -c'_ = will give the number of characters  
10. _**'tac'**_ = it is 'cat' in reverse :smiley:
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

1. ls: list files and folders that are not hidden.   
2. ls -a: list all files and folders that are hidden (_Hidden files begin with a '.'_). 
3. ls -l: list files and folders with long format and also shows permissions. 
4. ls -lh: same as 'ls -l' (_i.e. long format and permissions_) in addition shows readable size of each file.  
5. ls -lah: same as 'ls- lh' but also includes hidden files.  
6. ls -t: list the files and folders by date and time (descending order).  
7. ls -Glp: list files and folders with long format showing the type of file it is either a folder or file for example a txt file. 

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

1. ls -d $PWD/* : Lists directory with full path for each file or folder. 
2. ls -m : lists files and folders by comma separated.  
3. ls -g : list files and folders in long format but does not show owner name. 
4. ls -1 : list files and folders on separate lines. 
5. ls - R: list files and folders with subdirectories (this one is evil :imp: not my favorite one but good to know now :smiley:). 


---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

It takes an input and executes a command for a repetitve procedure For example in the command below it will list all the txt files and read the beginning 2 line of each text file in a particular directory

_ls *.txt | xargs head -2_
_find *.sh | xargs -J {} mv {} scriptingexamples/_
