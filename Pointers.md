### 1. Write a Program to print the address of variables using the address operator.
~~~c
#include <stdio.h>

int main() {
    int a;
    printf("Address=%p",&a);
}
~~~
### Output
~~~c
Address=0x7ffff03c0f1c
~~~
### 2. Write a program to print size of pointer variables.
~~~c
#include <stdio.h>

int main() {
    int *a;
    short *s;
    char *c;
    printf("Size of int pointer: %zu\n",sizeof(a));
    printf("Size of short pointer: %\zu",sizeof(s));
    printf("Size of char pointer: %zu",sizeof(c));
    
}
~~~
### Output
~~~c
Size of int pointer: 8
Size of short pointer: 8
Size of char pointer: 8
~~~
###  3. Write a program to print size of pointer variables and size of values Dereferenced by them.
~~~c
#include <stdio.h>

int main() {
    int *ptr_int;
    float *ptr_float;
    char *ptr_char;
    double *ptr_double;

    printf("Size of int pointer: %zu bytes\n", sizeof(ptr_int));
    printf("Size of value pointed by int pointer: %zu bytes\n\n", sizeof(*ptr_int));

    printf("Size of float pointer: %zu bytes\n", sizeof(ptr_float));
    printf("Size of value pointed by float pointer: %zu bytes\n\n", sizeof(*ptr_float));

    printf("Size of char pointer: %zu bytes\n", sizeof(ptr_char));
    printf("Size of value pointed by char pointer: %zu bytes\n\n", sizeof(*ptr_char));

    printf("Size of double pointer: %zu bytes\n", sizeof(ptr_double));
    printf("Size of value pointed by double pointer: %zu bytes\n", sizeof(*ptr_double));

    return 0;
}
~~~
### Output
~~~c
Size of int pointer: 8 bytes
Size of value pointed by int pointer: 4 bytes

Size of float pointer: 8 bytes
Size of value pointed by float pointer: 4 bytes

Size of char pointer: 8 bytes
Size of value pointed by char pointer: 1 bytes

Size of double pointer: 8 bytes
Size of value pointed by double pointer: 8 bytes
~~~
