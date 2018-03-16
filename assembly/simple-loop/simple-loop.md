# Creating a Simple Loop

With high level languages, it's easy to take even the simplest things for granted. In this exercise you will write assembly code that initializes an "array" of characters using an array. Consider the following c function:

```c
#include "stdio.h"

int main() {
  char a[10];
  for (int i=0; i<10; i++){
    int v = i + 48;
    a[i] = (char)v;
  }

  printf("%s", a); // prints 0123456789
}
```

> Do not worry about making a "function" called main. Simply write a `.asm` file which has the same behavior when executed as the C code inside the `main` function above. There is no need to implement a "calling convention" for this exercise. 

# Important Considerations

* How can we represent an array in assembly language?
  * What is the "data type" of the value being stored at each array index?
  * Where shall we store each of the characters?
  * How long shall each character be?
  * How does the concept of "null termination" play into this code?
* How can we use `syscall` to emulate our particular use of `printf`?
* How do we let "printf" know that it should be printing "0123456789" instead of "4849505152535455565758"

### Stretch It:

Once you have a working solution that prints 0123456789, how would you have to change your solution to print the integer values (rather than the ASCII characters) stored in our "array"?
