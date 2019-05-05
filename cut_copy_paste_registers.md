# Register Types
--------------
- Unnamed
- Numbered
- Named


* Registers proceeded with a double quote  ""

##  Unnamed
    - ""  the register used for cut-copy-paste operations - holds text from d, c, s, x, and y operations
                       * c = change command,   s = substitute command
    * Note: the first numbered register "0 also holds the last yanked text (y)


## Numbered registers = "0, "1 ... "9  

    - "0 holds the last yanked text (y)
    - "1 holds the delete (d) or changed (c) text
    * Note: with each succesive delete or change Vim shifts the text from register 1 into register 2 until 9 and then falls out of the register.


### To view register contents:


Type      :reg

#### STDOUT
--- Registers ---
""   TODO^J    * NOTE: the unnamed register

"0   TODO^J    * NOTE: also contains the yanked text as well because register 0 always contains the text from the most recent yank operation.

"1   ^J        * NOTE: ^J  represents a newline character

"2   ^J


#### After a delete command register 1 contains the most recent deleted text.

:reg
--- Registers ---
""   This line needs to be fixed at some point in the future.^J    * NOTE:  unnamed register
"0   TODO^J                                                        * NOTE:  still contains the most recent YANKED text
"1   This line needs to be fixed at some point in the future.^J    * NOTE: register 1 contains the most recent deleted text.
"2   ^J
"3   ^J


PUT the most recent YANKED text you must proceed the put command with the number of the register
-------------------------------

"0P  - will put the text from register 0 (TODO) into the line iwth the cursor.




The Black Hole Register   = /dev/null
-----------------------

"_     = when writing to the Black Hole register nothing happens.
         * NOTE: Used to delete text without affecting the normal registers.






