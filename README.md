#repeat

##NAME

    repeat - repeat a command n times with the possibility to define and use a counter

##SYNOPSYS

    repeat [OPTIONS] N COMMAND [ARGUMENT]...

##DESCRIPTION

    OPTIONS:

        -I replace-str
            Replace occurrences of replace-str in the command-arguments with the counter.

        -h
            Display usage

    N: number of repetition

    COMMAND [ARGUMENT]...: the command and its arguments to call

##EXAMPLES

    $ ./repeat 3 ls a 'b c'
    ls: cannot access 'a': No such file or directory
    ls: cannot access 'b c': No such file or directory
    ls: cannot access 'a': No such file or directory
    ls: cannot access 'b c': No such file or directory
    ls: cannot access 'a': No such file or directory
    ls: cannot access 'b c': No such file or directory

    $ ./repeat -I {} 3 ls a 'b c{}'
    ls: cannot access 'a': No such file or directory
    ls: cannot access 'b c0': No such file or directory
    ls: cannot access 'a': No such file or directory
    ls: cannot access 'b c1': No such file or directory
    ls: cannot access 'a': No such file or directory
    ls: cannot access 'b c2': No such file or directory

##AUTHOR

    Written by Jean-François Giraud.

##COPYRIGHT

    Copyright © 2021 Jean-François Giraud.  License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
    This is free software: you are free to change and redistribute it.  There is NO WARRANTY, to the extent permitted by law.

