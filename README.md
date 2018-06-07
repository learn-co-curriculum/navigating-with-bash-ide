## Navigating the Terminal

## Problem statement

As a developer, you spend a lot of time on your computer. You've already
learned about how the terminal allows you to interact with your computer on a more
granular level. Right now, when you open a file on your computer, you locate it
by navigating through the directories on your computer's file system using the
Finder (Mac) or File Explorer (Windows). Every file on your computer is stored
in your computer's file system, including files on your Desktop.

In previous lessons we stated that the terminal (or shell) was just another way
of working with the files and directories in your development environment. You
might be thinking: "Wait, how is this black screen with a command prompt
anything like the Finder or Windows Explorer I've been using for years?" In
this lesson we're going to show you how to translate tasks you've normally done
in a windowed environment to the terminal.

A note about terminology: you might see many different words that refer to the
black box portion in the lower right-hand section of the IDE. It can be called
a shell, BASH, command line, command prompt, console, or terminal. In Learn, we
will refer to it as a `terminal`, but if you see those other words and phrases
elsewhere, you'll know they all refer to the same thing.

![IDEterminal](https://s3.amazonaws.com/learn-verified/ILE-Console.png)

The terminal in your IDE allows you to access all of the files associated with
the code labs you're working through on Learn. This terminal provides you with
a "Command-Line Interface (CLI)" to navigate and operate on the files and
folders in the IDE.

Let's learn to navigate the files and folders on your IDE's terminal using the
following commands: `pwd`, `ls`, and `cd`. These commands are standards for almost 
all terminals (not just for your IDE).

## Objectives

1. Use `pwd` to identify the current directory of your terminal.
2. Use `ls` to list the files in the current directory of your terminal.
3. Use `cd` and `cd ..` to change directories in your terminal.

## Use `pwd` To Identify The Current Directory Of Your Terminal

When you open the IDE, your terminal is opened to a particular directory in the
file system. When you execute a program or do other work in your terminal, that
action happens in the context of a folder, or "directory".

This directory refers wherever you are on your IDE's file system when you run a
command in your terminal like `learn hello`. You did that from somewhere. This
somewhere is your _current directory_.

Open your IDE and in your terminal, you'll be at your terminal's _command-line
prompt_, where your computer is waiting for instructions.

### What's a Command Line Prompt?

Click on the Sandbox button in the upper right-hand corner of the lesson. This
will bring up a test environment where you can try out new commands and
concepts as you move through the course. Here, our command line prompt is
represented by:

```
[16:19:43] (master) Development
// ♥
```

The first line, `[16:19:43] (master) Development` is telling us the current
time, our current Git branch (master), and our current directory,
`Development`. What a "Git branch" is isn't important now. What's important is
that your prompt can be customized to give you helpful information about your
shell environment.

The next line, `// ♥` is also part of our command line prompt, where we can
type instructions and commands for our computer to execute. `// ♥` is a
customized prompt that we use here at Learn. To us the symbols `// ♥` remind us
of the way, '//', of love, '♥'. That's our mantra when we're programming. And
we think it looks pretty cool given how much time we spend in our terminals.

More generally, the command line prompt is represented by a `$`.  If you've
read other tutorials, you might be familiar with seeing command line
instructions with a `$` to represent the prompt. We try to follow this
convention in our instructions but you might sometimes see `// ♥` in images or
code samples.

What can you do from a command line prompt? Everything and anything. A command
line prompt is one of the most powerful interfaces in the world, from which
every computer and piece of software can be created, controlled, molded,
manipulated, and used!

### `pwd` - Print Working Directory

How do we know which directory our terminal is in? Let's run the following
command line program.

Type `pwd` and press Enter in your terminal in your Sandbox. You should see
something like:

```
// ♥ pwd
/home/cjbrock/Development
[16:19:43] (master) Development
// ♥
```

Here we typed `pwd` and pressed Enter on my keyboard. The terminal responded
with `/home/cjbrock/Development` and returned me to my current directory,
`Development` and gave me a new prompt, `♥`.

That's the standard procedure when you execute anything in a terminal. You enter
a command from a prompt in a directory, see output, and are returned to a new
prompt in your directory.

The `pwd` command is an acronym for "Print Working Directory." The `pwd`
command prints the working directory of your terminal session, the folder you
are currently "in."

Knowing which directory you are working within is crucial when using your
terminal. You are opening files and running programs that live in directories
and you need to make sure you're in the right directory for your task.

You never need to guess, if you're ever curious where you are or need to
confirm you are where you think you are, type `pwd`.

Why is it so crucial to know which directory you're in? Well, if you execute
the "delete all files in this directory" (a mere 5 key-strokes!) and you're in
the _wrong_ directory, the results can be _catastrophic_. Many prompts (like
you see above) constantly print out the working directory for safety. If a
prompt is _not_ set up to tell you where you are, you need `pwd`.

## Use `ls` to list the files in the current directory of your terminal.

Within a directory, one thing you're probably curious about is "which files or
other directories are contained here?". You can list everything in your
directory by executing `ls`:

```
[16:20:13] (master) Development
// ♥ ls
README.md
[16:20:13] (master) Development
// ♥
```

When we type `ls` in terminal, we're asking our terminal to list the files and
folders in the current working directory.

In the example above, typing `ls` in the `Development` directory shows you
there's a file named `README.md` contained within it.

## Use `cd` and `cd ..` to change directories in your terminal.

Now that you know how to print your current directory and see what's contained within it, you may be wondering: how do we move around to other directories and change our directory? The answer is with the `cd` command, which stands for Change Directory.

Try the following:

1. In your sandbox, click on the "Create New" button in the lower left-hand corner.
2. Choose the "Folder" option.
3. Name your folder `test`.
4. Now, from the `Development` directory, try:

```
// ♥ cd test
[16:19:43] test
// ♥
```

From within `Development`, at our prompt `♥`, we type `cd test`. Our terminal
will change the directory and enter our `test` folder and our prompt will now
indicate that our working directory is `Development/test`. It's that simple.
Confirm with: `pwd`. `pwd` should output something like:
`/home/cjbrock/Development/test`, the full path to your test directory.

### `..` and `.`

How do you move from `test` back up to your `Development` directory? You can
always move out of the current folder and back into the parent folder by typing
`cd ..`.  `..` is a shortcut that always means "the directory above" or the
"parent directory" of the current. Your file system is a tree like structure,
with directories being inside other directories:

```
├── Development
    ├── test
```

`test` is within `Development`. From within `test`, you would refer to the
parent directory, `Development` as `..`.

In the same manner that `..` means the directory above, the shortcut `.` means
the current directory. You'll see why being able to refer to your current
directory as `.` is helpful later in the course.

### Hint: Tab Autocomplete

When you're in terminal, to autocomplete a directory or a command, start typing and then press TAB.

## Key Terms

- terminal
- Command Line prompt
- `pwd`
- `ls`
- `cd`
- `cd ..`


<p class='util--hide'>View <a href='https://learn.co/lessons/navigating-with-bash-ide'>Navigating with BASH </a> on Learn.co and start learning to code for free.</p>
