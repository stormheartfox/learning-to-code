## Introduction to command line basics

### Navigating the terminal

Upon opening the terminal you will find yourself at the users home folder - delineated by a ```~``` in your prompt.

To list the files and folders in the directory you are currently in use the command:

```ls```

To list all files and folders including hidden files:

```ls -a```

Lets navigate into a folder then back to home as a practice.
The command you need to change directory is:

```cd```

Using this by iteself will yield no results as the terminal
does not know where you would like to change directory to,
lets choose one of the folders from your list you called earlier.
Try executing the command:

```cd Downloads```

You should see that the prompt now says ```~/Downloads```

This shows you have moved into a new folder. If you run ```ls``` again you will be able to see the files listed in your Downloads folder.


To move up one folder in the directory structure:

```cd ..``` 

Try navigating around your folders by using cd to to traverse up and down through your folders.
If at any time you're not sure where you are and want to return to your home folder use:

```cd ~```

You can also navigate through multiple folder layers by using the full path, e.g if you are in your Music folder and want to go straight to your downloads folder you can use:

```cd ~/Downloads```

This is the path from your home directory at ```~``` and down into the Downloads folder without having to type ```cd``` twice or more.