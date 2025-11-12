# Single Header File Dynamic Arrays

This dynamic array is a stupid simple dynamic array because I hate using C++ std library.
The array is just a simple struct with a len and cap with a buffer of whatever the type is.

### Example usage

```
#include <stdio.h>//or <cstdlib or whatever>

#include "dynarray.h"

int main(void){
  Dyn_Arry<int> arr = <int>new_dynarray(100) //allocates space for 100 elements not bytes
  for (int i = 0; i < 100;i++){
    arr.append(i); // pushes to back
  }
  printf("%d",arr[1]); //brackects can only be used to retreive data they cannot augment the buffer
  arr.free(); //frees all
}

```
