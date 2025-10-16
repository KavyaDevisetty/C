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
### 2. Write a program in C to read n number of values in an array and display them in reverse order.
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
    printf("Elements of array in the reverse order are:");
    for(int i=n-1;i>=0;i--)
    {
        printf("%d ",a[i]);
    }
    
}
~~~
### Output
~~~c
Enter the size of array:5
Enter elements of array:1 2 3 4 5
Elements of array in the reverse order are:5 4 3 2 1 
~~~
###  3. Write a program in C to find the sum of all elements of the array.
~~~c
// Online C compiler to run C program online
#include <stdio.h>

int main() {
    int a[50],n,sum=0;
    printf("Enter the size of array:");
    scanf("%d",&n);
    printf("Enter elements of array:");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    for(int i=0;i<n;i++)
    {
        sum+=a[i];
    }
    printf("Sum = %d ",sum);
    
}
~~~
### Output
~~~c
Enter the size of array:5
Enter elements of array:1 2 3 4 5
Sum = 15 
~~~
###  4. Write a program in C to copy the elements of one array into another array.
~~~c
#include <stdio.h>

int main() {
    int a[50],b[50],n,sum=0;
    printf("Enter the size of array:");
    scanf("%d",&n);
    printf("Enter elements of array:");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    for(int i=0;i<n;i++)
    {
        b[i]=a[i];
        
    }
    printf("Copied Elements are:");
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
Copied Elements are:1 2 3 4 5
~~~
### 5. Write a program in C to count the total number of duplicate elements in an array
~~~c
#include <stdio.h>

int main() {
    int a[50],n,count=0;
    printf("Enter the size of array:");
    scanf("%d",&n);
    printf("Enter elements of array:");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    for(int i=0;i<n;i++)
    {
        for(int j=i+1;j<n;j++)
        {
            if(a[i]==a[j])
            {
                count++;
                break;
            }   
        }
    }
    printf("No of duplicate elements in the array is:%d",count);
}
~~~
### Output
~~~c
Enter the size of array:6
Enter elements of array:1 2 2 3 2 3
No of duplicate elements in the array is:3
~~~
###  6. Write a program in C to print all unique elements in an array.
~~~c
#include <stdio.h>

int main() {
    int arr[100], n, i, j, count;

    printf("Enter number of elements in array: ");
    scanf("%d", &n);

    printf("Enter %d elements: ", n);
    for(i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("Unique elements are: ");
    for(i = 0; i < n; i++) {
        count = 0;
        for(j = 0; j < n; j++) {
            if(arr[i] == arr[j] && i != j) {
                count++;
                break;  // stop if duplicate found
            }
        }
        if(count == 0) {
            printf("%d ", arr[i]);
        }
    }

    printf("\n");
    return 0;
}

~~~
### Output
~~~c
Enter number of elements in array: 5
Enter 5 elements: 1 2 3 4 1
Unique elements are: 2 3 4
~~~
