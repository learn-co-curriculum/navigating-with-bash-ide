## Navigating with BASH

## Objectives

1. Explain how the Learn IDE (Integrated Development Environment) mimics the behavior of the shell 
2. Use `pwd` to identify the current directory of your IDE session
3. Use `ls` to list the files in the current directory of your IDE session
4. Use `cd` and `cd ..` to change directories in your IDE session. 


## Overview

When you open a file on your computer, you locate it by navigating through the directories on your computer's file system using Finder. Even files on your Desktop that you click on are stored in your computer's file system.

When you open an application from your Finder or Desktop, it always happens from the context of a "Working Directory" - the directory of your computer you were in when you executed the program. When you click on a file on your Desktop or Open an application from Your Dock or Applications directory, you are still opening a file in a directory. The Dock and Desktop are just abstractions for that directory to make them easy to access.

We're used to navigating and operating on these files using our GUI, or Graphical User Interface, provided by OS X (Macintosh) or whatever operating system we're using (e.g. Windows).

The shell (or Terminal) in your IDE allows you to access all of the files associated with the code labs you're working through on Learn. This Terminal provides you with a Command Line Interface to navigate and operate on the files and folders in the IDE. This is sometimes faster and easier than using the GUI. 

Let's learn to navigate the files and folders on your IDE's Terminal using the following commands. These commands are standards for all shells (not just for your IDE).

## `pwd` and Working Directories

When you open the IDE, your Terminal is open to a particular directory of the file system. When you execute a program or do other work in your Terminal, that action happens in the context of a "Working Directory."

A "Working Directory" just means wherever you are on your IDE's file system when you run a command in your Terminal like `learn hello`. You did that from somewhere. We call that somewhere, wherever you currently are, a "Working Directory".

Open your IDE and in your terminal, you'll be at your Command Line prompt, where your computer is waiting for instructions.

## What's a Command Line Prompt? 

Our Command Line prompt, and maybe yours if you configured your environment through Learn, is represented by:

```
[16:19:43] code
// ♥
```

The first line, `[16:19:43] code` is telling us the current time, so expect that part to be different for you, and our current working directory, `code`. (This is different from our Home directory which we'll explain later in this lesson.)

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

Here we typed `pwd` and pressed Enter on the keyboard. The terminal responded with `/home/AnnJohn/code` and returned me to my current directory, `code` and gave use a new prompt, `♥`.

That's the standard procedure when you execute anything in Terminal. You enter a command from a prompt in a working directory, see output, and are returned to a new prompt in your working directory.

The `pwd` command is an acronym for "Print Working Directory." The `pwd` command prints the working directory of your Terminal session, the folder you are currently "in."

Knowing what directory you are working within is crucial when using your Terminal. You are opening files and running programs that live in directories and you need to make sure you're in the right directory for your task.

You never need to guess, if you're ever curious where you are or need to confirm you are where you think you are, type `pwd`.

## `code` - Your Home Directory

When you signed up for Learn, we created a new workspace for you (labeled with your Github username) and a default directory called `code`, which is where all of your code will live. 

So that's what you're seeing when you see the directory `/home/AnnJohn/code`(here the user's name is AnnJohn, yours will be different!)

## `ls` - Listing Files in a Directory

Within a directory, one thing you're probably curious about is "what files or other directories are contained here?". You can list evertying in your working directory by executing `ls`:

```
[16:20:13] code
// ♥ ls
labs
[16:20:13] code
// ♥ 
```

When we type `ls` in Terminal, we're asking our Terminal to list the files and folders in the current working directory. 

In the example above, typing `ls` in the `code` directory, shows you there's another directory called `labs` contained within it. When you start solving code labs very soon, this is where they'll be stored.

## `cd` - Changing Directories

Now that you know how to print your working directory and see what's contained within it, you may be wondering: how do we move around to other directories and change our working directory? The answer is: with the `cd` command, which stands for Change Directory.

From the `code` directory, try:

```
// ♥ cd labs
[16:19:43] labs
// ♥
```

From within `code`, at our prompt `♥`, we type `cd labs`. Our terminal will change the directory and enter our `labs` folder and our prompt will now indicate that our working directory is `code/labs`. It's that simple. Confirm with: `pwd`. `pwd` should output something like: `/home/AnnJohn/code/labs`, the full path to your labs directory.

### `..` and `.`

How do you move from `labs` back up to your `code` directory? You can always move out of the current folder and back into the parent folder by typing `cd ..`. Two dots,  `..`, are a shortcut that always means "the directory above" or the "parent directory" of the current. Your file system is a tree like structure, with directories being inside other directories:

```
├── code
    ├── labs
```

`labs` is within `code`. From within `labs`, you would refer to the parent directory, `code` as `..`.

In the same manner that `..` means the directory above, the shortcut `.` means the current directory. You'll see why being able to refer to your current directory as `.` is helpful in a minute.

### Hint: Tab Autocomplete

When you're in Terminal, to autocomplete a directory or a command, start typing and then press TAB.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/navigating-with-bash-ide'>Navigating with BASH IDE</a> on Learn.co and start learning to code for free.</p>

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/navigating-with-bash-ide'>Navigating with BASH </a> on Learn.co and start learning to code for free.</p>
