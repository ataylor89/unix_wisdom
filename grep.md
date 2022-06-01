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