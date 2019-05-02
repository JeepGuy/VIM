# Deleting Text in Vim

In Command Mode:
----------------

   x  (lowercae) - Delete the single character that the cursor is on.
      - In insert mode the delete key works
   X (uppercase) - Delete the singel character that is before the coursor position

Commands in Vim:
---------------

operation{motion}
----------------

dw

d = The delete operation

w = The word motion

d l = delete the character under the cursor
      which is the same as the lowercase x
      x is basically a shortcut for d l 

d h = delete the character before the cursor
      same as Capital X (uppercase x)

d j = delete the current line AND the line beneath the one you are on.
      because the j is the line down key (the motion) 

d k = delete the current line AND the line above the current one you are on.
      because the k is the line up key (the motion where k would take you) 

d 0 = delete from the current position to the beginning of the line.
      (d zero) because 0 takes you to the front of the existing line.

d $ = delete from the current position to the end of the line.
      Because $ takes you to the end of the existing line. 

D   = capital D is . shortcut for d $ so this does the same thing as d $ immediately above.

dd  = delete the current line, regardless of your cursor position.

# dd = deletes the number of lines that the octothorpe (#) represents
       3dd would delete 3 lines of text after the current line.

[count]operator{motion}
------------------------

 5dw

5 = The count / how many times to repeat.

dw = The command (delete word)

3w = Repeat word motion 3 times

d3w = Delete the 3w motion.
      Same as 3dw = 3 times dw (delete word)

2d3w = Delete the 3 words two times
       Should use d6w or 6dw.

The Dot Operator
----------------

 .  = To repeat the last operation as many times as you want. 

 !  = 3 functions: force an action. Toggle a setting, use external commands.

 u  = undo last command







