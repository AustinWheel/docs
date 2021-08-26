---
Title: "Arrays"
Subjects:
  - "Code Foundations"
  - "Computer Science"
Tags:
  - "Arrays"
  - "Lists"
  - "Variable Types"
CatalogContent:
  - "learn-c-plus-plus"
  - "paths/computer-science"
---

In the C language, an array is a list of values, with a fixed length.  

## Declaring an Array

The syntax for declaring an array is first the array type, then the array name followed by square brackets surrounding the array's length (number of items):

```pseudo
type name[length];
```

So to declare an `int` array named `nums` with a length of 5:

```c
int nums[5]; // An array to hold five integers
```

Alternatively, the length can be omitted and the array's initial values can be assigned to it instead. Values are assigned inside of the curly brackets and separated by commas.

```c
int nums[] = {1, 2, 3, 4, 5};
```

## Accessing Values

The values in arrays are accessed using their index, or their position in the array. They can either be assigned or used this way.

```c
#include <stdio.h>

int main(void) {
  int nums[] = {1, 2, 3, 4, 5};
  
  printf("%d\n", nums[0]);
  
  nums[3] = 17;
  printf("%d\n", nums[3]);

  return 0;
}
```

The output would be:

```shell
1
17
```

Note that in C an array's indexes start at 0 instead of 1 like someone might expect.

```c
char letters[] = {'a', 'b', 'c', 'd', 'e'}; 
```

```pseudo
      +-----------------------+
Index | 0    1    2    3    4 |
      +-----------------------+
Value |'a'  'b'  'c'  'd'  'e'|
      +-----------------------+
```

So `letters[0]` will give use the value `'a'`.