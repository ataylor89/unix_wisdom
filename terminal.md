# Terminal

## How do I open Terminal?

Terminal might already be installed on your dock. If not, you can find it by opening Finder, navigating to the Applications folder, navigating to the Utilities folder, and double-clicking on Terminal.

Once the Terminal application launches, it will show up in the Dock.

To keep Terminal in the dock, you can right-click the Terminal icon, select options, and select "Keep in Dock".

## How does Terminal work?

The operating system (Mac OS) has an event loop. It listens for events in the event queue, and handles events when needed.

The operating system handles system-level events. An example would be a swipe on the trackpad. Another example would be when the user's mouse pointer goes to the top of the screen. When the pointer goes to the top of the screen, Mac OS shows the menu bar. The menu bar includes app menus, as well as status menus, Spotlight, Siri, the day and time, the control center, and the notification center. A third example is when the mouse pointer goes to the bottom of the screen. When the mouse pointer goes to the bottom of the screen, Mac OS shows the dock.

When an event is at the application level, the operating system passes control to the current application. In this case it's Terminal. So for keypresses and mouse clicks, Mac OS often passes control to Terminal. 

Terminal has an event loop just like Mac OS. Terminal listens for events in the event queue, and when it hears an event, calls the appropriate event handler.

When the return key is pressed, Terminal knows that the user has finished typing a command. Terminal reads the command from the text area, and passes the command to bash or zsh to be interpreted.

Terminal is a graphical user interface (GUI) that uses a shell program like bash or zsh to interpret commands.

You can find out which shell program Terminal is using by typing

    echo $0

or

    echo $SHELL

in Terminal.

When Terminal gets output from its shell program (often bash or zsh) it displays that output on the screen. 

Thus the underlying shell program (bash or zsh) is an interpreter that Terminal uses to interpret commands or shell scripts.

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