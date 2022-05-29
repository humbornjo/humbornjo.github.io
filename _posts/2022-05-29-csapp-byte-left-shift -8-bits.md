## Byte shift for 8 bits

### There are two results when shifting an 8-bit number 8 positions to the left according to 15-213.

1. zero
2. unchanged

Logically, it should be zero, but in intel machine 

```c
#include<stdio.h>

int main(){
  int a=768;
  printf("int a<<32 = %d\n",a<<32);
}
```
result remains 768.

#### Think about "<< 7" for a Byte width value
Byte is promoted to 16 bit(2 Byte) and is multiplied by 128(which is exactly <<7 means). Then the result is converted with the 16 bits value module 256. The first 7 bit in the original Byte value disappeared because (2^n * 128) mod 256 = 0, where n is positive integer.
 
same thing happens to "<< 8", 256 mod 256 = 0, that's where 1.zero comes from.

#### Why not change 
In most occasions, the number of shifted bits is less than the width of the value. So the shift instruction shifts the value in the 8-bit register or memory argument by 8 & 7 => 1000 & 0111 = 0 positions. 

Consider <<7, 7 & 7 = 7, everything makes sense.



