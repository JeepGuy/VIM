# VIM Cut Copy Paste commands

- Move text around in a file
- Duplicate text
- Make an in-file backup
- Reuse the same text

The same operation{motion} pattern applies in Cut Copy Paste in Vim
    - [count]operator{motion}


d and x cut text, not delete it

cut = delete and save into a register

Register is a clipboard-like storate location

* In the Command Mode
---------------------

CUT Operator = delete in other editors
---------------------------------------

x    - delete a single character

dd   - Using dd cuts a line of text and places it in the unnamed register - sometimes called the default register


PASTE Operator = put in Vim
---------------------------
       
p    - put command (lowercase p) = "paste" (Vim referrs to this as the put command ) ~ roughly equal to "paste"
     - puts the text from the unnamed register into the line (location) AFTER  where the cursor is. 
                                                          e.g. the line below the current cursor position

P    - P (uppercase) puts the text before your cursor.


ddp  - swap lines  * that is dd cuts the text and p pastes the text on the line below the current line (cursor location)
                   
COPY Operator = yank in Vim
---------------------------

y    - yank 

yw  - yank a word
y$  - yank to the end of the line

2yw - yank two words

yy  - yanks an entire line


4yy - yanks 4 lines

****   to paste any of the text in the above examles use p (put the text on the line below) or P (put the text on the line above).


UNDO Command
-------------

u  - undos the last change

Contrl r  - Redo  





