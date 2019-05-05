# Register Types

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
    * Note: with each succesive delete or change Vim shifts the text from register 1 into register 2 until 9 
      and then the text falls out of the register.


### To view register contents:

```
:reg

#### STDOUT
--- Registers ---
""   TODO^J    
            * NOTE: the unnamed register
"0   TODO^J 
           * NOTE: also contains the yanked text because register 0 contains the text from the most recent yank operation.
"1   ^J    
           * NOTE: ^J  represents a newline character
"2   ^J
```

#### After a delete command register 1 contains the most recent deleted text.

```
:reg

#### STDOUT
--- Registers ---
""   This line needs to be fixed at some point in the future.^J    * NOTE:  unnamed register
"0   TODO^J
            * NOTE:  still contains the most recent YANKED text
"1   This line needs to be fixed at some point in the future.^J
           * NOTE: register 1 contains the most recent deleted text.
"2   ^J

"3   ^J
```

#### PUT the most recent YANKED text you must proceed the put command with the number of the register

oP  - (zero P) will put the text from register 0 (TODO) into the line iwth the cursor.


### The Black Hole Register   = /dev/null

"_     = (quote underscore)  when writing to the Black Hole register nothing happens.
         * NOTE: Used to delete text without affecting the normal registers.



## Named Registers

 - There are 26 named registers, from a - z
 - You can specify a register when yanking or deleting, just as you can when you are putting (pasting)

"ayy  - will yank the line into register "a" 
   - which is represented by doubel quote a     "a

You can see the line yanked in register a below:

```
:reg
--- Registers ---
""   Put this line in the a register.^J
"0   This line needs to be fixed at some point in the future.^JYou're work is not quite finished...^JThis line needs to be fixed at some point in the future.^J
"1   This line needs to be fixed at some point in the future.^J
"2   ^J
"3   ^J
"4   ^J
"5   :help :help<ENTER>^J
"6   You can even get help with :help.^J
"7   You can also get help on a given subject:^J
"8   You can specify a command to get help with, too.^J
"9   ^J
"a   Put this line in the a register.^J
"w   wwwwbbbbwwwwwbbbbbbbbWWWWWWWBBBBBBBggG1gg3G:44^M:$^M:44^M^G^G:$^Mgg^G^H^G^Gg^[^[^[^[^[^[:1G^M{;
"-   y
":   reg
"%   cutcopypaste.txt
"/   \<Create\>

```
 
Yanking the next line will show be displayed in register b.

```
:reg
--- Registers ---
""   Put this one in the b register.^J
"0   This line needs to be fixed at some point in the future.^JYou're work is not quite finished...^JThis line needs to be fixed at some point in the future.^J
"1   This line needs to be fixed at some point in the future.^J
"2   ^J
"3   ^J
"4   ^J
"5   :help :help<ENTER>^J
"6   You can even get help with :help.^J
"7   You can also get help on a given subject:^J
"8   You can specify a command to get help with, too.^J
"9   ^J
"a   Put this line in the a register.^J
"b   Put this one in the b register.^J
"w   wwwwbbbbwwwwwbbbbbbbbWWWWWWWBBBBBBBggG1gg3G:44^M:$^M:44^M^G^G:$^Mgg^G^H^G^Gg^[^[^[^[^[^[:1G^M{;
"-   y
":   reg
"%   cutcopypaste.txt
"/   \<Create\>

```

#### You can put (paste) with the named register

"aP   - will paste from the a register

"bP   - will paste form the b register 

After both put operations the registers show:

```
:reg
--- Registers ---
""   Put this one in the b register.^J
"0   This line needs to be fixed at some point in the future.^JYou're work is not quite finished...^JThis line needs to be fixed at some point in the future.^J
"1   This line needs to be fixed at some point in the future.^J
"2   ^J
"3   ^J
"4   ^J
"5   :help :help<ENTER>^J
"6   You can even get help with :help.^J
"7   You can also get help on a given subject:^J
"8   You can specify a command to get help with, too.^J
"9   ^J
"a   Put this line in the a register.^J
"b   Put this one in the b register.^J
"w   wwwwbbbbwwwwwbbbbbbbbWWWWWWWBBBBBBBggG1gg3G:44^M:$^M:44^M^G^G:$^Mgg^G^H^G^Gg^[^[^[^[^[^[:1G^M{;
"-   y
":   reg
"%   cutcopypaste.txt
"/   \<Create\>

```


#### Append more text to the register
 -  use the Capital Letter as in "A  or "B

"Ayy   - will append the new line to the existing a register.

You can see below that the line was appended to the existing text in the a register.

If you were to have used lowercase a then the text would have been replaced.

```
:reg
--- Registers ---
""   Put this one in the b register.^JAppend this line to the b register.^J
"0   This line needs to be fixed at some point in the future.^JYou're work is not quite finished...^JThis line needs to be fixed at some point in the future.^J
"1   This line needs to be fixed at some point in the future.^J
"2   ^J
"3   ^J
"4   ^J
"5   :help :help<ENTER>^J
"6   You can even get help with :help.^J
"7   You can also get help on a given subject:^J
"8   You can specify a command to get help with, too.^J
"9   ^J
"a   Put this line in the a register.^JAppend this line to the a register.^J
"b   Put this one in the b register.^JAppend this line to the b register.^J
"w   wwwwbbbbwwwwwbbbbbbbbWWWWWWWBBBBBBBggG1gg3G:44^M:$^M:44^M^G^G:$^Mgg^G^H^G^Gg^[^[^[^[^[^[:1G^M{;
"-   y
":   reg
"%   cutcopypaste.txt
"/   \<Create\>
```

#### Can be used with delete operations

"wzdw  - will delete the word at the cursor into the w register.

```
:reg
--- Registers ---
""   This
"0   This line needs to be fixed at some point in the future.^JYou're work is not quite finished...^JThis line needs to be fixed at some point in the future.^J
"1   This
"2   This line needs to be fixed at some point in the future.^J
"3   ^J
"4   ^J
"5   ^J
"6   :help :help<ENTER>^J
"7   You can even get help with :help.^J
"8   You can also get help on a given subject:^J
"9   You can specify a command to get help with, too.^J
"a   Put this line in the a register.^JAppend this line to the a register.^J
"b   Put this one in the b register.^JAppend this line to the b register.^J
"w   This
"-   y
":   w
"%   cutcopypaste.txt
"/   \<Create\>

```






