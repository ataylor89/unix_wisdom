# grep 

## What does grep mean?

The name grep means "globally search for a regular expression and print matching lines".
The name comes from the command g/re/p, a command used in the ed text editor.

## How do I use grep?

grep comes preinstalled on Unix, Linux, and Mac OS

## What are some examples of grep?

Let's say you're a programmer and you want to search a directory tree of source code and configuration files for a specific word (like the name of a module, method, class, image or file). 

And let's make the scenario even more specific.

Suppose you're a programmer and you're thinking about removing an image from your Git repository. Do any HTML pages use this image or include this image? If you remove the image prematurely, you might have an image missing from your website and it might be conspicuous to the user.

What's the name of this image file? Let's call it "old_logo.png".

You can search for old_logo.png in your HTML files with the following command.

    grep -nrw . -e "old_logo.png"

This command searches every file in the current directory, and every subdirectory, for the pattern "old_logo.png". It then prints the search results, preceding each match with the line number of the match.

You might ask, why are there so many options? The -nrw string specifies three options. The -e string specifies a fourth option. What do these options mean?

Let's go over every option.

<pre>
grep –nrw . -e <pattern> 

-n, --linenumber: each output line is preceded by its relative line number in the file 
-r, --recursive: recursively search subdirectories listed (grep behaves as rgrep) 
-w, --word-regexp: the expression is searched for as a word  
-e pattern (--regexp=pattern): an input line is selected if it matches any of the specified patterns 
</pre>

Thus the command means: Search for this pattern as a word, in this directory and every subdirectory, and include line numbers in each search result.

## What's another example of grep?

Above we discuss a complicated (but very helpful) usage of grep. We searched every file in a directory and its subdirectories for a pattern.

Let's now consider a simpler usage.

Let's say we have the file index.html. We want to see if the image logo.png appears in the file index.html.

We can search for this pattern with the following grep command:

    grep 'logo.png' index.html

In this example, we use the same syntax but without the options. 

Why is it the same syntax? 

It's because the standard syntax for a Unix command is 

    command -options arguments

In the first example (in the previous section) we passed options, and the options took on arguments.

    grep –nrw . -e 'old_logo.png'

In the second example (in the current section) we pass arguments.

    grep 'logo.png' index.html

The standard syntax for grep is:

    grep -options [pattern] [file(s)]

So the command <pre>grep 'logo.png' index.html</pre> passes a pattern and a file as arguments. 

The command <pre>grep –nrw . -e 'old_logo.png'</pre> passes options and their arguments.

## The syntax for a grep command

We can find the syntax for a grep command in the man page, under the synopsis section.

    grep [-abcdDEFGHhIiJLlMmnOopqRSsUVvwXxZz] [-A num] [-B num] [-C[num]] [-e pattern] [-f file] [--binary-files=value] [--color[=when]] [--colour[=when]] [--context[=num]] [--label]
            [--line-buffered] [--null] [pattern] [file ...]

## What else is in the man page?

A lot more! 

The man page has a detailed description of the grep command and all of its options. It also has examples of using grep to search for patterns and regular expressions.

The man page describes grep in this way (first line of the description):

    The grep utility searches any given input files, selecting lines that match one or more patterns.

It then goes on to say:

    grep is used for simple patterns and basic regular expressions (BREs); egrep can handle extended regular expressions (EREs).

So grep is used for searching patterns and regular expressions. 

The grep utility can search a file, or every file in a directory, or every file in a directory tree, for a pattern or regular expression.

## Is there more in the man page?

Of course there is.

We discussed (above) how the man page has a synopsis section, a description section, and an examples section.

The man page also has a history section.

The history section informs us:

    The grep command first appeared in Version 6 AT&T UNIX.

We can use grep on Unix, Linux, Mac OS and many other operating systems. The grep command comes preinstalled on Unix, Linux and Mac OS. The grep utility is a standard Unix utility. Both Linux and Mac OS are derived from Unix. So grep is a standard utility on Linux and Mac OS as well.

## Can we search a pattern without the -e option?

Of course we can. In the second example we did just that.

    grep 'logo.png' index.html

Now let's say you want to search a directory tree for the same pattern.

We can do this with the command

    grep -nrw 'logo.png'

The -r option takes a list of directories. When there are no directories listed, it defaults to the current directory. Thus the current directory is implied. 

The string 'logo.png', in quotes, is the pattern supplied as an argument to the grep command.

Thus the commands

    grep -nrw 'logo.png'

and

    grep -nrw . -e 'logo.png'

mean the same thing. 

The second command explicitly states the directory we are searching. It also uses the -e option.

## Why do we even have the -e option?

It's simple. You can pass multiple -e options and search for multiple patterns.

From the grep man page

    Specify a pattern used during the search of the input: an input line is selected if it matches any of the specified patterns.  This option is most useful when multiple -e options are used to specify multiple patterns, or when a pattern begins with a dash (‘-’).

Now, if you tried to specify multiple patterns without using the -e option, the grep command would be confused, and it would interpret a pattern you give it to be the name of a file.

Thus the -e option is very useful. 

## Options create syntax

In unix commands, options create syntax.

The syntax of a word is its function in a sentence. We can extend this to Unix commands. The syntax of a word in a Unix command is its function in the command.

The -e option specifies the syntax of the word that follows. The word that follows is a pattern that grep is instructed to search for. 

## grep is a utility, a command, and a language

The grep command has its own vocabulary and grammar. 

A language is a pairing of grammar and vocabulary.

Thus grep is a command, a utility, and a language.

We could say that every standard Unix command has its own language.

The Unix command-line has a standard grammar and vocabulary. 

    command -options arguments

A grammar is a set of rules. A vocabulary is a set of words.

Thus the Unix command-line has a standard grammar and vocabulary. This standard makes it easier to learn how to use Unix commands on the command-line.

## What about shells?

The shell program (a command-line interface) is a Unix utility that has its own grammar and vocabulary. An example would be IO redirection (the < << >> > symbols) and pipelining (the | symbol).

We use the shell program as an intermediary to grep because the shell program adds functionality. For example, we can redirect the search results of a grep search to file.

    grep 'logo.png' index.html > search_results.txt

The shell program also allows us to create and define enviroment variables.

Some examples of shells are bash and zsh.

We can also find out what shell we are using with the commands

    echo $0

and

    echo $SHELL

Unix shells have a standard syntax just like Unix command-line utilities. The shell programs bash and zsh both understand IO direction operators and the pipe operator. 

The pipe operator allows us to chain processes. For example

    ls -l | sort

The above command sorts the output of ls -l. The commands ls and sort are connected by a pipe.

Another example would be

    ls -als ~ | grep -e .zprofile -e .zsh -e .bash

The above command searches our home directory for the configuration files .zprofile, .zsh*, and .bash_profile.

Literally, it searches the output of ls -als for the patterns .zprofile, .zsh, and .bash.

You can see that the search results are different when we pass the -w option to grep.

    ls -als ~ | grep -w -e .zprofile -e .zsh -e .bash

The -w option searches for the patterns as words, giving us different search results.

In these examples we have chained processes together by use of the pipe symbol (|). This shows the power and flexibility of shell programs like zsh and bash, which facilitate usage of standard Unix software, like ls, sort, and grep.

## What's Terminal?

If you're using Mac OS, and you're typing grep commands into Terminal, you might wonder, what is Terminal?

Terminal is a graphical user interface (GUI) that has an underlying shell program (zsh or bash). The underlying shell program is a command-line interface (CLI).

So Terminal is a GUI. Bash is a CLI. Zsh is a CLI.

You might wonder, in what way is Bash a CLI? In what way is Zsh a CLI?

Well, you can write a program in C, C++, C#, Java, Python, or another programming language that opens a process as a file (from the operating system's perspective, a process is a file) and communicates with the process. In the same way that you can use C, Java, or Python to open a file, read from a file, and write to a file, you can use these languages to open a process, write to a process, and read from a process.

Thus a program written in C, Java or Python can open the bash and zsh processes, write to them, and read to them. You can write your own GUI to interact with a shell like bash or zsh. 

Terminal is a standard GUI that comes with Mac OS that allows users to interact with a shell like bash or zsh.

## Shells in more detail

Shells allow us to interact with an operating system's software through a command-line interface. The Unix, Linux, and Mac OS operating systems come with preinstalled shells like bash or zsh. These operating systems then ship GUIs that interact with the underlying shell. The Terminal application is a GUI that interacts with bash or zsh and comes preinstalled with Mac OS.

The purpose of shells is to provide a user with a command-line interface. The shell program interprets the user's commands and thus acts as an interpeter. 

An analogy would be Python.

Python comes with an interpreter that interprets Python commands.

We use Terminal to interact with Python. Python then interprets our commands.

In the same way, we use Terminal to interact with a shell program. The shell program (like bash or zsh) then interprets our commands. It can interpret IO direction (the symbols < << > >>) pipelining (the symbol |) and more. It can also define environment variables that we can use. It can also store state information in a configuration file (like .zprofile or .bash_profile).

Thus we see software interacting with software, or software interacting with software interacting with software.

    Terminal > zsh > grep
    Terminal > zsh > python 

The programs zsh, bash, and Python are all interpreters. 

Thus shell programs are interpreters, just like python and java are interpereters.

The GUI (Terminal) is separate from the interpreter. 

The GUI (Terminal) sends user input to interpreters like bash, zsh, and Python.

## Are shells really intepreters, like python and java?

Of course they are. That's why you can write shell scripts. The shell interprets every line in a shell script, the same way Python and Java interpret every line in a Python file or a Java file.

## So are bash and zsh programming languages?

They are. Bash and Zsh are languages just like Python and Java.

Bash and Zsh are often called shell scripting languages.

Shell scripting languages follow many standards and have a standard syntax.

Bash and Zsh are programming languages and you can write shell scripts (programs) and pass them to Bash and Zsh.

## So when we run grep in Terminal, what are we really doing?

Terminal is a Mac OS application. At the basic level, it's a process.

The Terminal application interacts with a shell process (bash or zsh).

The shell process then interacts with the operating system's software (like ls sort grep python java).

Thus Terminal talks to shell, and shell talks to grep.

Terminal > shell > grep

Terminal is a graphical user interface (GUI). The shell program is a command-line interface (CLI). And grep is a standard unix utility that takes options and arguments as input and produces output.

Terminal provides a graphical layer (a GUI). Shell provides a command-line interface (a CLI) that interprets user commands. It's literally an interface just like a Java interface is an interface. The grep utility is a program that searches files for patterns, and it accepts patterns and files as inputs, and produces search results as an output.

## Summary

The grep utility searches input files for a pattern or a regular expression. The grep utility can search a single file, every file in a directory, or every file in a directory tree. The standard syntax of the grep command is

    grep pattern file(s)

We can use grep by opening Terminal on Mac OS, or by opening a terminal emulator on Unix or Linux.

In addition, we can write our own GUI in place of Terminal, and use our own GUI to interact with shell or even to interact with grep alone. We can also write a program in C, Python or Java that interacts with grep.

If you type

    whereis grep

you get the location of grep.

    % whereis grep
    /usr/bin/grep

Now you can get the permissions for grep.

    % ls -l /usr/bin/grep
    -rwxr-xr-x  1 root  wheel  173440 Jan 1  2012 /usr/bin/grep
    
The first column gives you file permissions. The second gives you the number of hard links. The third and fourth give you the owner and group associated with the file. The fifth column gives you the file size. The sixth column gives you the date and time of the last modification to the file. The seventh column gives you the filename.

From the file permissions, we see that any user of the operating system can use the grep utility.

The first three-letter group (rwx) represents permissions for root. The second three-letter group (r-x) represents permissions for wheel. The third three-letter group (r-x) represent permissions for all users. 

Thus all users of the operating sytem have read (r) and run (x) permissions to /usr/bin/grep.

This means that your software can run grep from any user account, if you write software that communicates with the grep process.

The file permission representation (-rwxr-xr-x) is a standard representation of file permissions by the ls program and across many operating systems (like Unix, Linux, and Mac OS).

That tells you where grep is on your system (in the /usr/bin directory), what grep's file permissions are (-rwxr-xr-x).

You might ask, when I type "grep" my computer associates it with /usr/bin/grep. Why is that?

It's because the shell program you use (bash or zsh) has the string /usr/bin in its PATH variable. Thus it searches /usr/bin for the grep program when you type "grep" into Terminal.

This way you don't have to type /usr/bin/grep every time. You can use the shorthand "grep", because the path /usr/bin is stored in the PATH variable as one of many standard paths.

## A more concise summary

The grep program lets us search a file (or files) for one or more patterns. The grep program first appeared in an early version of Unix (Version 6 AT&T UNIX) and is a standard service in Unix, Linux and Mac OS.

The standard syntax of grep is

    grep pattern file(s)

We can also use grep with options, e.g.

    grep -nrw pattern

The above command searches all files in the directory tree (recursively) for the specified pattern. It prints the line number of matching lines and searches for the pattern as a word.

## Addendum

grep is a program. Shell is a program and an interpreter. Python is a program and an interpreter. Thus we can see an analogy between shell and python and java: they are all interpreters.

When you learn shell, you learn a programming language (also called a scripting language). grep is a useful word in the shell scripting language. grep is so standard that it's really a part of the Unix shell.

Since Mac OS and Linux are based on Unix, grep is also a part of Mac OS and Linux shells.

grep is a standard utility in the Unix, Linux, and Mac OS shells.

## A second addendum

Why do they call shell shell?

It's because a Unix shell is, conceptually, the outermost layer of the operating system, which provides access to the operating system's software.

As a reminder, the program grep is named after the command g/re/p, a command in the text editor ed, which searches globally for a regular expression and prints matching lines.

That's where shell and grep get their names.