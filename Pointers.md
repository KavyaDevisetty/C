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
### 7. Write a program to print postfix/prefix increment/decrement in a pointer variable of base type int*.
~~~c
#include <stdio.h>

int main() {
    int a[5] = {10, 20, 30, 40, 50};
    int *ptr;

    ptr = a; // pointer points to the first element

    printf("Initial pointer address: %p, value: %d\n\n", ptr, *ptr);

    // --- Postfix increment ---
    printf("Postfix increment (ptr++):\n");
    printf("Address before increment: %p, value: %d\n", ptr, *ptr);
    ptr++;
    printf("Address after increment: %p, value: %d\n\n", ptr, *ptr);

    // --- Prefix increment ---
    printf("Prefix increment (++ptr):\n");
    ++ptr;
    printf("Address after increment: %p, value: %d\n\n", ptr, *ptr);

    // --- Postfix decrement ---
    printf("Postfix decrement (ptr--):\n");
    printf("Address before decrement: %p, value: %d\n", ptr, *ptr);
    ptr--;
    printf("Address after decrement: %p, value: %d\n\n", ptr, *ptr);

    // --- Prefix decrement ---
    printf("Prefix decrement (--ptr):\n");
    --ptr;
    printf("Address after decrement: %p, value: %d\n", ptr, *ptr);

    return 0;
}

~~~
### Output
~~~c
Initial pointer address: 0x7fff9113dbe0, value: 10

Postfix increment (ptr++):
Address before increment: 0x7fff9113dbe0, value: 10
Address after increment: 0x7fff9113dbe4, value: 20

Prefix increment (++ptr):
Address after increment: 0x7fff9113dbe8, value: 30

Postfix decrement (ptr--):
Address before decrement: 0x7fff9113dbe8, value: 30
Address after decrement: 0x7fff9113dbe4, value: 20

Prefix decrement (--ptr):
Address after decrement: 0x7fff9113dbe0, value: 10
~~~
### 8.  Write a Program to print the value and address of  elements of an array using pointers notation.
~~~c
#include <stdio.h>

int main() {
    int a[5] = {10, 20, 30, 40, 50};
    int *ptr;
    int i;

    ptr = a; 

    printf("Value and Address of Array Elements using Pointer Notation:\n\n");

    for (i = 0; i < 5; i++) {
        printf("Element %d: Value = %d\t Address = %p\n", i, *(ptr + i), (ptr + i));
    }

    return 0;
}

~~~
### Output
~~~c
Value and Address of Array Elements using Pointer Notation:

Element 0: Value = 10	 Address = 0x7ffe3eb1ded0
Element 1: Value = 20	 Address = 0x7ffe3eb1ded4
Element 2: Value = 30	 Address = 0x7ffe3eb1ded8
Element 3: Value = 40	 Address = 0x7ffe3eb1dedc
Element 4: Value = 50	 Address = 0x7ffe3eb1dee0
~~~
### 9. Write a program to print the value of array elements  using pointers and subscript notation.
~~~c
#include <stdio.h>

int main() {
    int a[5] = {10, 20, 30, 40, 50};
    int *ptr;
    int i;

    ptr = a; // pointer points to the base address of the array

    printf("Printing array elements using Pointer and Subscript Notation:\n\n");

    for (i = 0; i < 5; i++) {
        printf("Element %d:  *(ptr + %d) = %d\t ptr[%d] = %d\n", i, i, *(ptr + i), i, ptr[i]);
    }

    return 0;
}
~~~
### Ouput
~~~c
Printing array elements using Pointer and Subscript Notation:

Element 0:  *(ptr + 0) = 10	 ptr[0] = 10
Element 1:  *(ptr + 1) = 20	 ptr[1] = 20
Element 2:  *(ptr + 2) = 30	 ptr[2] = 30
Element 3:  *(ptr + 3) = 40	 ptr[3] = 40
Element 4:  *(ptr + 4) = 50	 ptr[4] = 50
~~~

### 10. Write a program to print the value and address of array elements by subscripting  a pointer variable.
~~~c
#include <stdio.h>

int main() {
    int a[5] = {10, 20, 30, 40, 50};
    int *ptr;
    int i;

    ptr = a; // pointer points to the base address of the array

    printf("Printing Value and Address of Array Elements using Pointer Subscript Notation:\n\n");

    for (i = 0; i < 5; i++) {
        printf("Element %d: Value = %d\t Address = %p\n", i, ptr[i], &ptr[i]);
    }

    return 0;
}

~~~
### Output
~~~c
Printing Value and Address of Array Elements using Pointer Subscript Notation:

Element 0: Value = 10	 Address = 0x7ffefe1f6a90
Element 1: Value = 20	 Address = 0x7ffefe1f6a94
Element 2: Value = 30	 Address = 0x7ffefe1f6a98
Element 3: Value = 40	 Address = 0x7ffefe1f6a9c
Element 4: Value = 50	 Address = 0x7ffefe1f6aa0
~~~
