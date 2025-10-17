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

### 4. Write a program to illustrate the dereferencing of pointers.
~~~c
#include <stdio.h>

int main() {
    int a = 25;       
    int *ptr;         
    ptr = &a;         

    printf("Value of a: %d\n", a);
    printf("Address of a: %p\n", &a);
    printf("Address stored in ptr: %p\n", ptr);
    printf("Value pointed by ptr (dereferenced value): %d\n", *ptr);

    // changing value using pointer dereferencing
    *ptr = 50;
    printf("\nAfter modifying value using pointer:\n");
    printf("New value of a: %d\n", a);
    printf("Value pointed by ptr: %d\n", *ptr);

    return 0;
}

~~~
### Output
~~~c
Value of a: 25
Address of a: 0x7ffcade0c2d4
Address stored in ptr: 0x7ffcade0c2d4
Value pointed by ptr (dereferenced value): 25

After modifying value using pointer:
New value of a: 50
Value pointed by ptr: 50
~~~
###  5. C program to illustrate pointer arithmetic
~~~c
#include <stdio.h>

int main() {
    int a[5] = {10, 20, 30, 40, 50};
    int *ptr1, *ptr2;

    ptr1 = a;       // points to the first element (a[0])
    ptr2 = &a[3];   // points to the fourth element (a[3])

    printf("Initial positions:\n");
    printf("ptr1 -> Address: %p, Value: %d\n", ptr1, *ptr1);
    printf("ptr2 -> Address: %p, Value: %d\n\n", ptr2, *ptr2);

    // --- Incrementing pointer ---
    ptr1++;  // moves to next element
    printf("After Incrementing ptr1 (ptr1++):\n");
    printf("Address: %p, Value: %d\n\n", ptr1, *ptr1);

    // --- Decrementing pointer ---
    ptr2--;  // moves one element back
    printf("After Decrementing ptr2 (ptr2--):\n");
    printf("Address: %p, Value: %d\n\n", ptr2, *ptr2);

    // --- Pointer addition ---
    ptr1 = ptr1 + 2;  // moves two elements ahead
    printf("After Adding 2 to ptr1 (ptr1 + 2):\n");
    printf("Address: %p, Value: %d\n\n", ptr1, *ptr1);

    // --- Pointer subtraction ---
    ptr1 = ptr1 - 1;  // moves one element back
    printf("After Subtracting 1 from ptr1 (ptr1 - 1):\n");
    printf("Address: %p, Value: %d\n\n", ptr1, *ptr1);

    // --- Pointer difference ---
    int diff = ptr2 - ptr1;
    printf("Difference between ptr2 and ptr1: %d elements\n", diff);

    return 0;
}

~~~
### Output
~~~c
Initial positions:
ptr1 -> Address: 0x7fffbfdd0a60, Value: 10
ptr2 -> Address: 0x7fffbfdd0a6c, Value: 40

After Incrementing ptr1 (ptr1++):
Address: 0x7fffbfdd0a64, Value: 20

After Decrementing ptr2 (ptr2--):
Address: 0x7fffbfdd0a68, Value: 30

After Adding 2 to ptr1 (ptr1 + 2):
Address: 0x7fffbfdd0a6c, Value: 40

After Subtracting 1 from ptr1 (ptr1 - 1):
Address: 0x7fffbfdd0a68, Value: 30

Difference between ptr2 and ptr1: 0 elements
~~~
###  6. Write a program to declare an integer variable a, assign it a value, then declare a pointer variable, assign it the address of a, and finally print the value of a using the pointer variable.
~~~c
#include <stdio.h>

int main() {
    int a = 10;
    int *p;
    p=&a;
    printf("Value = %d",*p);

 
}
~~~
### Output
~~~c
Value = 10
~~~
