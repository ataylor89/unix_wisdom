# ls

## What is ls?

The command ls lists the files in a directory. ls is short for "list". We can pass ls different options to specify the format of the output.

## What are some formats?

We can use the default format

    ls /usr/local

We can also use the long format

    ls -l /usr/local

## How can I see files that begin with a dot?

Many configuration files begin with a dot and are hidden from the ls output.

We can see these files with the -a option.

    ls -al ~
    ls -al ~ | grep -e '.zprofile' -e '.bash_profile'

The first example (above) lists all files in our home directory.

The second example (above) searches for the hidden files .zprofile and .bash_profile in our home directory.