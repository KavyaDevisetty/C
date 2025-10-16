###  1. Write a program in C to store elements in an array and print them.
~~~c
#include <stdio.h>

int main() {
    int a[50],n;
    printf("Enter the size of array:");
    scanf("%d",&n);
    printf("Enter elements of array:");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("Elements in the array are:");
    for(int i=0;i<n;i++)
    {
        printf("%d ",a[i]);
    }
    
}
~~~
### Output
~~~c
Enter the size of array:5
Enter elements of array:1 2 3 4 5
Elements in the array are:1 2 3 4 5 
~~~
