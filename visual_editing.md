# Visual mode

Use v to start characterwise visual mode.
Use V to start linewise visual mode.
Use Ctrl-v to start blockwise visual mode.

You can use motions to expand the visual area.
You can also use text objects to expand the visual area.

Just some of commands you can use in visual mode include:
~ - Switch case
c - Change
d - Delete
y - Yank
r - Replace
x - Delete
I - Insert
A - Append
J - Join
u - Make lowercase
U - Make uppercase
> - Shift right

---

### The "till" command = t{} 
   - For instance: till the next letter capital "D" woudl be:

        tD (in command mode) and the cursor will jump to the next Capital D in the buffere (text).
---
### Yank this (inner sentence) sentenance YIS
   - This places the words into the unnamed register.
   * check it via:    :reg "


---
## To transform text

### To put all lines of text on a single line. 

   * Start off by placing your cursor anywhere on the first line:
   * Next, enter linewise visual mode by typing V. (capital v)
   * Select the entire paragraph with ip, which stands for inner paragraph. 
   * Finally, join all the lines with the join command by typing " j " 

### To capitalize text and then center it. 

   - Position cursor on the line to transform.
   - Enter linewise visual mode - type  " v "
   - Select the current line ( and the next line by typing " j " )
   - Change all to Uppercase by typing " U "  

### To re-select the lines above type   gv 

   - To center the lines above, highlight them using gv
   - then type:    " :center" and press enter 

# Blockwise Visual Mode
 - sometimes called vertical Visual mode...

## Add a comment to a group of lines.

- Move the cursor to the first word in the line to start visual block editing...
- enter visual block mode   Control - v   ( from command mode)
- navigate downward to the lines to add comment to... HJKL
- Insert the # symbol by typing capital I followed by space then escape (wait for a moment)


# This is a comment.
# So is this.
# Why, this is also a comment.
# Please, comment us out!



