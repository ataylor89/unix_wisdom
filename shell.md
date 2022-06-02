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

One use of the grep command is

    grep pattern file(s)

This usage of grep searches for a pattern in the file or files listed.

We can also use grep to search for text in every file of a directory and its subdirectories.

    grep -nrw pattern

This usage of grep searches for a pattern in every file of the directory tree.

The man command brings up the manual page for any Unix command. The syntax is

    man command

For example,

    man ls
    man echo
    man grep

We often call the manual page the "man page" as an abbreviation.

The man page has many sections, including a synopsis, a description and more. The man page often has a section with examples and a section on the history of the command.

## Where does shell gets its name?

The word shell often refers to the outermost layer of something. 

The user interface of an operating system can be thought of as its outermost layer.

## What happens when I use Terminal?

The operating system (Mac OS) has an event loop that listens for events like keypresses, trackpad activity, and mouse clicks.

If any of these events are system-level events, the operating system handles these events.

If the events are application-level events, and Terminal is the currently selected application, the operating system passes control to Terminal.

Terminal has an event loop, just like the operating system, that listens for events in the event queue.

When Terminal hears an event, it handles the event.

When the return key is pressed, Terminal recognizes the end of a command, and parses the command. Terminal then passes the command to its underlying interpreter, bash or zsh, which produces output in response. 

Terminal displays this output on the screen.