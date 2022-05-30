## vi/vim number flow 

### Generate 1-100 every num occupies a single line.

#### 1. Macro record 
  i1<ESC>q<MACRO_NAME>yyp<CTRL-a>q98@<MACRO_NAME>
  1. i1<ESC>: input 1 in line 1 return normal
  2. q<MACRO_NAME>: start recording macro
  3. yyp: "yy" copy the line and "p" paste the copied line
  4. <CTRL-a>: "CTRL+a" increment the next number
  5. q: stop record
  6. 98@<MACRO_NAME>: execute the macro for 98 times
  
  MACRO_NAME is casual, name the macro 1, the sequence would be "i1<ESC>q1yyp<CTRL-a>q98@1"
  
  
#### 2. put/0put 
  put =range(1,100)
  or
  0put =range(1,100)
  
  refer to :h


#### 3. substitute
  99o<ESC>:%s/^/\=line(".")
  1. 99o<ESC>: add 99 empty line
  2. :%s: substitute all the document
  3. /: delimiter
  4. ^: start of the line
  5. /: delimiter
  6. \=: Evaluate
  7. line("."): return the number of the line
  
  About step 6&7, refer to :h line(), try it.
