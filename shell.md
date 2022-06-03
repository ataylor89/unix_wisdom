# shell

## What is a shell?

[Wikipedia](https://en.wikipedia.org/wiki/Shell_(computing)) gives this definition for a shell.

> In computing, a shell is a computer program which exposes an operating system's services to a human user or other programs. In general, operating system shells use either a command-line interface (CLI) or graphical user interface (GUI), depending on a computer's role and particular operation. It is named a shell because it is the outermost layer around the operating system.

The Macintosh operating systems have many unix shells, like bash and zsh, since Mac OS is a derivative of Unix. We can use these Unix shells by opening Terminal.

## How do I open Terminal?

Terminal might already be installed on your dock. If not, you can find it by opening Finder, navigating to the Applications folder, navigating to the Utilities folder, and double-clicking on Terminal.

Once the Terminal application launches, it will show up in the Dock.

To keep Terminal in the dock, you can right-click the Terminal icon, select options, and select "Keep in Dock"

## How do I use Terminal?

To use Terminal, we simply type commands and then press the return key.

For example, the command

    ls -l

lists the directory contents using the long format. The -l option specifies the long format.

The command

    ls -al

lists the directory contents, including filenames that begin with a dot, using the long format. The -a option specifies that ls should include filenames that begin with a dot.

The command

    grep -nrw 'hello world'

searches all files in the current directory, and every subdirectory, for the pattern "hello world".

The command

    grep 'python' ~/.zprofile ~/.bash_profile

searches the ~/.zprofile and ~/.bash_profile configuration files for occurrences of the pattern "python".

The command

    man grep

brings up the manual page for the Unix command grep. The manual page (or man page) has a synopsis of the command, and a description of the command. The man page often has a section with examples and a section on the history of the command.

## What's a shell scripting language?

Shell programs like bash and zsh are interpreters, just like python and java are interpreters.

Bash and Zsh are also programming languages, just like python and java are programming languages.

We often call them scripting languages, since we write scripts for bash and zsh. But a scripting language is a kind of programming language.

Thus shell is a scripting language, a programming language, and an interpreter. We can say the same about java and python. 

(Have you noticed that the latest versions of Java come equipped with jshell, which lets you write scripts in Java just like you can write scripts in Python?)

## Are there other definitions of shell?

There are.

The Wikipedia definition is a good one.

Another good definition is this: A shell is a user interface to an operating system. 

With this second definition, we can think of the Unix shell, the Windows shell, and the Macintosh shell as user interfaces to the respective operating systems.

This Markdown document provides two definitions of shell: the definition from Wikipedia and the second definition provided in this section. Both are interesting definitions.