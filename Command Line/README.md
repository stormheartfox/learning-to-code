# Introduction to command line basics

In this section you will learn the basics of how to utilise the terminal in a Mac/Linux system,
from navigation, to file and folder creation, adding text to files and deletion.

---
## Table of Contents:
- [Navigating the terminal](https://github.com/michaeljgrant/learning-to-code/tree/main/Command%20Line#navigating-the-terminal)
- [Creating files & folders](https://github.com/michaeljgrant/learning-to-code/tree/main/Command%20Line#creating-files-and-folders)
- [Deleting files & folders](https://github.com/michaeljgrant/learning-to-code/tree/main/Command%20Line#deleting-files-and-folders)
---
### Navigating the terminal

Navigating through your terminal is one of the most basic skills, when connecting to a remote machine or navigating your own local files, these skills are something everyone must know.

The commands used in this section are:

| Command         | Argument | Usage |
|-----|-----|--------|
| ls |   |List files & folders in the current directory|
|ls -a||List all files & folders in current directory, including hidden.|
| cd    |  foldername |Change directory into folder named|
|cd ~||Navigate to users home directory|
cd ..||Navigate up one level from current directory|



Upon opening the terminal you will find yourself at the users home folder - delineated by a ```~``` in your prompt.

To list the files and folders in the directory you are currently in use the command:

```ls```

To list all files and folders including hidden files:

```ls -a```

Lets navigate into a folder, list it's contents and then return back to your home directory as a practice.

The command you need to change directory is:

```cd```

Using this by iteself will yield no results as you have not given a directory to navigate to, by default cd will take you to your home directory,
lets choose one of the folders from your list you called earlier.
Try executing the command:

```cd Downloads```

You should see that the prompt now says ```~/Downloads```

This shows you have moved into a new folder. If you run ```ls``` again you will be able to see the files listed in your Downloads folder.


To move up one folder in the directory structure:

```cd ..``` 

Try navigating around your folders by using cd to to traverse up and down through your folders.
If at any time you're not sure where you are and want to return to your home folder use:

```cd```
or
```cd ~```

Both of these commands will return you to your home directory.


You can also navigate through multiple folder layers by using the full path, e.g if you are in your Music folder and want to go straight to your downloads folder you can use:

```cd ~/Downloads```

This is the path from your home directory at ```~``` and down into the ```Downloads``` folder without having to type ```cd``` twice or more.

---
### Creating files and folders

Now that you've learned how to navigate through your computer's folder structure, you can move onto the creation of files & folders.

The commands used in this section are:

| Command         | Argument | Usage |
|-----|-----|--------|
| touch |  filename.extension e.g newfile.txt |Create a new file in the current directory|
| mkdir      |  foldername |Create a new folder in the current directory|

From the terminal you are able to create new files and folders, the same as if you were creating them in the file explorer.

To create a new file we use the command:

```touch```

Followed by the name of the file we wish to create. All files have extensions, some of which you would be familiar with, ```.jpg``` for example, is a photo file. 
Lets create a new empty text file.

```touch mytextfile.txt```

This creates a new file called ```mytextfile.txt``` in your current directory. Try listing the contents of your current directory to see if you can find the file you just created.

Similarly we can also create new folders, sometimes called directories. 
To do this we use the command:

```mkdir```

Followed by the name of the folder we wish to create.

```mkdir mynewdirectory```

Will create a new folder with the name ```mynewdirectory``` in the users current directory. Try listing out the contents of your current directory and then navigating into the new folder.

If you list the contents of the directory you just created, you will notice it is empty. Try creating a new file here as well.

When creating files within different folders they can all have the same name. For example, when navigating into the newly created folder, you could create a new file named ```mytextfile.txt``` again, because it does not exist inside of this folder.

Similarly you can create another folder within your ```mynewdirectory``` folder called ```mynewdirectory``` and the system will not return an error.

You will get the following error if you try to create something that already exists in your current location:

```File exists```

Unlike in your file explorer the command line will not suggest adding a ```01``` to the end of a file, you will have to manually enter a unique name as an argument.

---
### Deleting files and folders

Having created a bunch of new folders & files in the previous section, you're probably asking yourself, how do I get rid of them?

In the following section we will utilise the remove commands to delete folders and files:

| Command         | Argument | Usage |
|-----|-----|--------|
|rm|filename| Delete named file|
|rm -rf| foldername| Delete directory named and all contents within|

Eventually, files and sometimes entire folders are no longer of use to us and need to be deleted from the system.

When deleting any files & folders we can use the ```rm``` command, for example if we wished to delete the ```mytextfile.txt``` file created in the previous section we would use:

```rm mynewtextfile.txt```

This will delete the file named. If you misspell the file name and no file with the misspelled name exists you will get the following error:

```No such file or directory```

Try deleting the ```mynewdirectory``` folder created in the previous section from your command line.

You should come across the following error:

```mynewdirectory: is a directory```

This is because the ```rm``` command by itself only deletes singular files. And requires additional flags to delete directories and their contents.

To delete a directory we use the flags ```r``` & ```f```, which forces the system to delete the folder and everything within it.

Use the following command to delete the created directory and it's contents:

```rm -rf mynewdirectory```

Now when you list the contents of your current directory you will see both the text file & the directory created in the previous section have been removed.

---