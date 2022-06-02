# shell

## What is shell?

Shell gets its name from the word shell, which can mean the outermost layer of something. The shell program on an operating system is the outermost layer of the operating system.

Shell is an interface to a computer. It's a very big interface to a computer, which gives you access to all of the files and software on a computer.

Shell is a command-line interface, abbreviated CLI. 

Shell is also a scripting language, a programming language, and an interpreter.

When you learn shell, you learn a scripting language.

When you learn shell, you learn a programming language.

(A script is a kind of program, and a scripting language is a kind of programming language.)

Shell is an interpreter just like python and java are interpreters.

Examples of shells are bash and zsh, which are commonly found on Unix and Mac OS.

## How can I use shell?

Shell is a command-line interface. bash and zsh are shells. But how do you interact with bash and zsh?

Let's go through it step by step.

You can interact with shell on Mac OS using Terminal.

When you type on your keyboard or make clicks on your trackpad, these events enter an event loop. The operating system listens for events in the event loop, and queues them, and handles them.

When Terminal is open, Terminal is notified of events like keypresses and mouse clicks.

Terminal gets user input from the keyboard and passes it to the underlying, which might be bash or zsh.

## Is Terminal a GUI or a CLI?

The answer is, both.

Terminal is both a GUI and a CLI.

Remember that shell is an interface. Terminal is an interface. Finder is an interface.

shell is a command-line interface (CLI). Finder is a graphical user interface (GUI). 

Terminal is both a command-line interface (CLI) and a graphical user interface (GUI).

The reason is simple. Terminal gives you a graphical user interface (like menus and menu items and a window wiht a scrollable text area). Terminal also gives you a command-line interface (via the underlying shell which interprets your commands).

Thus Terminal is both a GUI (graphical user interface) and a CLI (command-line interface).

Terminal affords you tremendous access to a computer (all of its files and software).

Finder similarly affords you tremendous access to a computer (all of its files and all of its applications).

Terminal and Finder are both interfaces to Mac OS, and to the computer running Mac OS.

Finder is a GUI. Terminal is both a GUI and a CLI.

## What's a step-by-step summary of how I use Terminal?

The operating system (Mac OS) listens for events in an event loop.

It picks up your keyboard input.

It passes your keyboard input to the process currently running (Terminal).

Terminal passes the command to the underlying shell (bash or zsh).

The shell interprets your command and produces output. 

Terminal picks up the output (by reading from the shell process) and prints the output on its text area.

Terminal reads from and writes to the shell process to interpret your commands, and prints the output of the shell program on its text area.

## Shell is a CLI. But is it a GUI?

Let's think about this. Terminal is both a GUI and a CLI. Shell is a CLI.

We can use shell without a graphical user interface.

We can use shell over voice recognition.

There are computers that have shell as software but don't have graphical user interfaces. They might have voice interfaces that interact with programs like shell.

So you can make a Unix computer that has no windows, keyboards, or mouse clicks, but instead relies on voice recognition that interacts with a command-line interface like shell.

It's kind of like this.

You can SSH into a computer over voice recognition. 

And that's a metaphor (we're comparing SSH to voice recognition).

You can speak a username and a password to a computer in order to log in.

You can speak commands to a computer that are recognized by voice recognition and interpreted by shell.

## Is there another way of explaining it?

CLI is a beautiful acronym as is GUI.

Really, shell is an interpreter and a scripting language. It's also a programming language.

When you think of shell as being analogous to python, it makes a lot of sense.

Shell is a scripting language, a programming language, and an interpreter.

When you learn shell, you learn a scripting language, a programming language, and an interpreter.

## Commands and shell scripts

We can write single commands to shell that are interpreted by shell.

    ls -als | grep .zprofile 

    ls -als | grep -e .zprofile -e .bash_profile -e .zsh

    grep -nrw <pattern>

    grep <pattern> <file>

We can also write shell scripts that are interpreted by shell.

    mkdir icons.iconset
    sips -z 512 512   $1 --out icons.iconset/icon_512x512.png
    cp $1 icons.iconset/icon_512x512@2x.png
    sips -z 512 512   $1 --out icons.iconset/icon_256x256@2x.png
    sips -z 256 256   $1 --out icons.iconset/icon_256x256.png
    sips -z 256 256   $1 --out icons.iconset/icon_128x128@2x.png
    sips -z 128 128   $1 --out icons.iconset/icon_128x128.png
    sips -z 64 64     $1 --out icons.iconset/icon_32x32@2x.png
    sips -z 32 32     $1 --out icons.iconset/icon_32x32.png
    sips -z 32 32     $1 --out icons.iconset/icon_16x16@2x.png
    sips -z 16 16     $1 --out icons.iconset/icon_16x16.png
    iconutil -c icns icons.iconset

The above shell script creates an icons.icns file from an image. The image filename is passed as an argument and stored as the variable $1.

## Summary

Shell is a scripting language, a programming language, and an interpreter.

Many operating systems come equipped with shells, like Unix, Linux, Mac OS and Windows.

Shell gets its name from the word shell, which can mean the outermost layer of something. A shell program on an operating sytem is the outermost layer of an operating system.

Shell programs give you a command-line interface to the files and software on an operating system.

You can interact with the default shell on a Mac OS computer by opening Terminal.