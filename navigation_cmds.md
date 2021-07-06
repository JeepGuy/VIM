Basic Navigation Commands: in command (command line) mode.

    h moves the cursor one character to the left.
    j moves the cursor down one line.
    k moves the cursor up one line.
    l moves the cursor one character to the right.

    0 moves the cursor to the beginning of the line.
    $ moves the cursor to the end of the line.
    ^ moves cursor to the beginning of line or selection at the first word (no the first space on CentOs7).
    w move forward one word.
    b move backward one word.
    G move to the end of the file. 3 G will take you to the third line in the file. 
    gg move to the beginning of the file. 3 gg will take you to the third line in the file as well.
    `. move to the last edit.
    :$ move to last line in file
    :<line #> moves to a specific line number>
    <Ctrl> g  - show how many lines are in file.
    <Ctrl> f   aka Page-down  To move forward one page in the file.  Hold down the control key and press "f".
    <Ctrl> b   aka Page-up    To move backward in the file. Hold down the control key and press "b".

    ^f  - gets the help file definition for <Cntrl> f

    CTRL-F                  Scroll window [count] pages Forwards (downwards) in
                        the buffer.  See also 'startofline' option.
                        When there is only one window the 'window' option
                        might be used.  

    CTRL-B                  Scroll window [count] pages Backwards (upwards) in the
                        buffer.  See also 'startofline' option.
                        When there is only one window the 'window' option
                        might be used.

Expanded Definitions for above.
-------------------------------

To move down a line:  press "j"

To move up a line:  press "k"

To move to the right:  press "l"
  
To move to the left:   press "h"  

To repeat a move, press and hold down the key.

----------------------

Ctrl-f   aka Page-down  To move forward one page in the file.  Hold down the control key and press "f".

Ctrl-b   aka Page-up    To move backward in the file. Hold down the control key and press "b".
 

: <line Number>   = colon and the line number  -  jumps to a specific line in a file
                  To move to line 32, you would type ":32<ENTER>".
                  To go to the last line, use ":$<ENTER>".

w  (lowercase)   Move forward by word. To use white space as word boundaries, use uppercase "W".

b  (lowercase)    Move backward by word. To use "b". To use white space as word boundaries, use uppercase "B".

gg (lowercae)     Move to the begining of the file, or "1gg"  (numeral one and gg = 1gg)

:<line #> moves to a specific line number.

G  (uppercase)    Move to the last line of the file, type "$G" or just "G"

<LINE_NUMBER>gg or <LINE_NUMBER>G     To go to a specific line number.  

z <enter>         Move the lines up on the screen but leaves the cursor at the same position in the document


For info on the file type Cntrl G

To list the line number and column on a file you set the ruler:
-----------------------

:set ruler

:set no ruler to turn of the option
     can append an exclaimation mark to an option to make it toggle - able

:set ruler! (switches to the opposed mode each time used - first time on second time off)

You can use some regular expressions

^ = beginning of line or selection  - Shift 6 (caret)
$ = end of line or selection

