# shell

## What is shell?

One formal definition of shell is the user interface of an operating system.

When we speak of the Unix shell, we speak of the Unix user interface.

There is also the Windows shell and the Macintosh shell. 

The user interface of an operating system (the shell) consists of the graphical user interface (GUI), the command-line interface (CLI), voice recognition, face recognition, and more.

Part of learning the Unix shell, the Windows shell, or the Macintosh shell is learning the command-line interface of the operating system.

## How can I use the command-line interface?

On Mac OS, you can use the command-line interface by opening Terminal. If Terminal is not already in your Dock, you can store Terminal in Dock for easy access.

In Terminal, you can type a command like

    ls -l

and get a listing of the directory contents.

To end the command, press the return key. 

When you press the return key, Terminal recognizes the end of a command and interprets the command.

## How does Terminal work?

Terminal is a GUI that has an underlying interpreter which interprets your commands. The underlying interpreter is often bash or zsh, two derivatives of sh.

If you'd like to find out which interpreter Terminal is using, you can run the commands

    echo $0

and

    echo $SHELL

in Terminal.

## What are some useful commands?

In this document we have used the ls and echo commands. 

We used the command

    ls -l

to get a listing of files in the current directory.

The -l option tells ls to use the long format.

We can also use the -a option, to list filenames that begin with a dot.

    ls -al

Many configuration files (like .zprofile and .bash_profile) have names that begin with a dot.

We used the commands

    echo $0

and

    echo $SHELL

to get the name of the interpreter we are using.

We can also use echo to write to a file.

    echo "Hello world" > helloworld.txt

The above command redirects the output of echo to the file helloworld.txt.

You might ask, what does echo really do?

Echo echoes input as output. It can be used to write to file. It can also be used in a shell script to display text on the screen.

In addition to ls and echo, there are the grep and man commands.

The grep command, which searches for patterns in files, is very useful, and is documented in the [grep.md Markdown file](https://github.com/ataylor89/unix_wisdom/blob/main/grep.md).

We can bring up the manual page for any Unix shell command by typing

    man <command>

For example,

    man ls
    man echo
    man grep

We often call the manual page the "man page" as an abbreviation.

The man page has many sections, including a synopsis, a description and more. The man page often has a section for examples and a section on the history of the command.

## Where does shell gets its name?

We defined shell as the user interface of an operating system.

The word shell often refers to the outermost layer of something. 

The user interface of an operating system can be thought of as its outermost layer.