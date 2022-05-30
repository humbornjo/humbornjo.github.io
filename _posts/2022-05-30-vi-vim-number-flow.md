## vi/vim number flow ##

### Generate 1-100 every num occupies a single line.##

#### 1. Macro record ####
  i1<ESC>q<MACRO_NAME>yyp<CTRL-a>q98@<MACRO_NAME>
  1. i1<ESC>: input 1 in line 1 return normal
  2. q<MACRO_NAME>: start recording macro
  3. yyp: "yy" copy the line and "p" paste the copied line
  4. <CTRL-a>: "CTRL+a" increment the next number
  5. q: stop record
  6. 98@<MACRO_NAME>: execute the macro for 98 times
  
  MACRO_NAME is casual, name the macro 1, the sequence would be "i1<ESC>q1yyp<CTRL-a>q98@1"
  
  
#### 2. put/0put ####
  put =range(1,100)
  or
  0put =range(1,100)
