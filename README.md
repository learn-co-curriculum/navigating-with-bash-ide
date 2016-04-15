## Navigating with BASH

## Objectives

1. Explain how the IDE mimics the behavior of the shell 
2. Use `pwd` to identify the current directory of your IDE session
3. Use `ls` to list the files in the current directory of your IDE session
4. Use `cd` and `cd ..` to change directories of your  Nitrous Console session


## Overview

When you open a file on your computer, you locate it by navigating through the directories on your computer's file system using Finder. Even files on your Desktop that you click on are stored in your computer's file system, your hard drive.

When you open an application from your Finder or Desktop, it always happens from the context of a "Working Directory" - the directory of your computer you were in when you executed the program. When you click on a file on your Desktop or Open an application from Your Dock or Applications directory, you are still opening a file in a directory. The Dock and Desktop are just abstractions for that directory to make them easy to access.

We're used to navigating and operating on these files using our GUI, our Graphical User Interface, provided by OS X (Macintosh) or whatever operating system we're using (Windows).

The terminal in your IDE doesn't allow you to access the files on your computer, but it does let you access all the files that you load on to your IDE. In other words, you can access all the labs that you load on to the IDE from Learn. This terminal provides us with a Command Line Interface to navigate and operate on the files and folders in our IDE. As programmers, the Terminal is our workbench, not the GUI.

Let's learn to navigate the files and folders on your IDE using the following commands. These commands are standards for all terminals (not just for your IDE).

## `pwd` and Working Directories

When you open the IDE, your Terminal is open to a location within a directory of the file system. Whatever programs you execute or work you do in your Terminal, that action happens in the context of a "Working Directory."

A "Working Directory" just means wherever on your IDE you are when you execute a program by running a command in your Terminal like `learn hello`. You did that from somewhere. We call that somewhere, wherever you currently are, a "Working Directory".

Open your IDE and in your terminal, you'll be at your Command Line prompt, where your computer is waiting for instructions.

## What's a Command Line Prompt? 

Our Command Line prompt, and maybe yours if you configured your environment through Learn, is represented by:

```
[16:19:43] code
// ♥
```

The first line, `[16:19:43] code` is telling us the current time, so expect that part to be different for you, and our current working directory, `code`. (This is different our Home directory which we'll explain later in this lesson.)

The next line, `// ♥` is our command line prompt, where we can type instructions and commands for our computer to execute. `// ♥` is a customized prompt that you got by setting up your environment through Learn. To us the symbols `// ♥` remind us of the way, '//', of love, '♥'. That's our mantra when we're programming. And we think it looks pretty cool given how much time we spend in our Terminal.

More generally, the command line prompt is represented by a `$`.

If you've read other tutorials, you might be familiar with seeing command line instructions with a `$` to represent the prompt. We try to follow this convention in our instructions but you might sometimes see `// ♥` in images or code samples.

What can you do from a command line prompt? Everything and anything. A command line prompt is the most powerful interface in the world, from which every computer and piece of software can be created, controlled, molded, manipulated, and used.

### `pwd` - Print Working Directory

Let's run the following command line program. 

Type `pwd` from your prompt. You should see something like:

```
// ♥ pwd
/home/AnnJohn/code
[16:19:43] code
// ♥
```

Here we typed `pwd` and pressed Enter on my keyboard. The terminal responded with `/home/AnnJohn/code` and returned me to my current directory, `code` and gave use a new prompt, `♥`.

That's the standard procedure when you execute anything in Terminal. You enter a command from a prompt in a working directory, see output, and are returned to a new prompt in your working directory.

The `pwd` command is an acronym for "Print Working Directory." The `pwd` command prints the working directory of your Terminal session, the folder you are currently "in."

Knowing what directory you are working within is crucial when using your Terminal. You are opening files and running programs that live in directories and you need to make sure you're in the right directory for your task.

You never need to guess, if you're ever curious where you are or need to confirm you are where you think you are, type `pwd`.

## `code` - Your Home Directory

When you open a new Terminal session, you start in a default location in your file system.


'/' means the main directory of your IDE. Every file and folder on your computer lives somewhere inside of `/`.

`/home` is the main  directory in the IDE. Within `/Users`, there is a folder for your username, the name of the Github account you used to login to your IDE. In this case, the username is `AnnJohn` so the home directory is: `/home/AnnJohn/code`. Yours will be different and you can see it by opening a new Terminal session and typing `pwd`.

`code` is the default directory in the IDE, whatever it may be. 

## `ls` - Listing Files in a Directory

Within a directory, one thing you're probably curious about is "what files are in this directory?". You can list files within your working directory by executing `ls`:

```
~ $ ls
Applications  Development   Desktop
Documents     Downloads     Public        		    
```

When we type `ls` in Terminal, we're asking our Terminal to list the files and folders in the current working directory.

In my home directory, `code`, there are 6 directories, `Applications`, `Development`, `Desktop`, `Documents`, `Downloads`, and `Public`. The directories you have in the IDE will only be the labs that you've downloaded on there. 

## `cd` - Changing Directories

When you open a new Terminal session, you'll be in a working directory, probably `code`. But how do we move around to other directories and change our working directory? You can use the `cd` command, which stands for Change Directory.

From the `code` directory, try:

```
// ♥ cd labs
[16:19:43] labs
// ♥
```

From within `code`, at our prompt `♥`, we type `cd labs`. Our terminal will change the directory and enter our `labs` folder and our prompt will now indicate that our working directory is `code/labs`. Your prompt might look a little different but you'll be in your `Desktop` directory. Confirm with: `pwd`. `pwd` should output something like: `/home/AnnJohn/code/labs`, the full path to your labs directory.

Once your working directory is labs, try `ls` and have your Terminal list any files that are in that directory.

### `..` and `.`

How do you move from `labs` back up to your `code` directory? You can always move out of the current folder and back into the parent folder by typing `cd ..`.  `..` is a shortcut that always means "the directory above" or the "parent directory" of the current. Your file system is a tree like structure, with directories being inside other directories:

```
├── code
    ├── labs
```

`labs` is within `code`. From within `labs`, you would refer to the parent directory, `code` as `..`.

In the same manner that `..` means the directory above, the shortcut `.` means the current directory. You'll see why being able to refer to your current directory as `.` is helpful in a minute.

### cd `~`

You can also change directory back to your home directory from anywhere via `cd ~`.  `~` is a shortcut that means home so if you type `cd ~` you are telling your terminal to change the working directory to your home directory. Try it now.

Then enter `ls` and you'll see the `code` directory. Go ahead and `cd` back into it. 

### Hint: Tab Autocomplete

When you're in Terminal, to autocomplete a directory or a command, start typing and then press TAB.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/navigating-with-bash-ide'>Navigating with BASH IDE</a> on Learn.co and start learning to code for free.</p>
