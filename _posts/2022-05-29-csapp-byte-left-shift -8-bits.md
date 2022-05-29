There are two results when shifting an 8-bit number 8 positions to the left. (Correct me if I'm wrong)

1. zero
2. unchanged


```c
#include<stdio.h>

int main(){
  int a=768;
  printf("a<<8 = %d\n",a<<32);
}
```
res is 768
