### 1.WRITE A C PROGRAM TO ACCEPT TWO INTEGERS AND CHECK WHETHER THEY ARE EQUAL OR NOT?
~~~c
#include<stdio.h>
int main()
{
  int a,b;
  printf("enter 2 integers:");
  scanf("%d %d",&a,&b);
  if(a==b)
    printf("Both are equal.");
  else
    printf("Both are not equal.");
  return 0;
}
~~~
### Output
~~~c
enter 2 integers:2 3
Both are not equal.
~~~

### 2.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS EVEN OR ODD?
~~~c
#include<stdio.h>
int main()
{
  int n;
  printf("Enter integer:");
  scanf("%d",&n);
  if(n%2==0)
    printf("Even number");
else
    printf("Odd number");
}
~~~
### Output
~~~c

Enter integer:2
Even number
~~~
###  3.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS POSITIVE OR NEGATIVE?
~~~c
#include<stdio.h>
int main()
{
  int n;
  printf("Enter number:");
  scanf("%d",&n);
  if(n>0)
    printf("Positive number");
  else
    printf("Negative number");
}
~~~
### Output
~~~c
Enter number:2
Positive number
~~~
### 4.WRITE A C PROGRAM TO FIND WHETHER A GIVEN YEAR IS A LEAP YEAR OR NOT?
~~~c
#include <stdio.h>

int main() {
    int year;

    // Input year from user
    printf("Enter a year: ");
    scanf("%d", &year);

    // Check leap year conditions
    if ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0)) {
        printf("%d is a leap year.\n", year);
    } else {
        printf("%d is not a leap year.\n", year);
    }

    return 0;
}
~~~
### Output
~~~c
Enter a year: 2000
2000 is a leap year.
~~~

### 5.WRITE A C PROGRAM TO READ THE AGE OF A CANDIDATE AND DETERMINE WHETHER HE IS ELIGIBLE TO CAST HIS/HER OWN VOTE
~~~c
#include<stdio.h>
int main()
{
  int age;
  scanf("%d",&age);
  if(age>=18)
    printf("Eligible To Cast his/her Vote");
  else
    printf("Not Eligible To Cast his/her Vote");
}
~~~
### Output
~~~c
Enter age: 19
Eligible To Cast his/her Vote
~~~
###  6.WRITE A C PROGRAM TO READ THE VALUE OF AN INTEGER M AND DISPLAY THE VALUE OF N IS 1 WHEN M IS LARGER THAN 0, 0 WHEN M IS 0 AND -1 WHEN M IS LESS THAN 0.
~~~c
#include<stdio.h>
int main()
{
  int m,n;
  printf("enter an integer:");
  scanf("%d",&m);
  if(m>0)
    n=1;
  else if (m<0)
    n=-1;
  else
    n=0;
printf("n is %d",n);
}
~~~
### Output
~~~c
enter an integer:9
n is 1
~~~
###  7.WRITE A C PROGRAM TO FIND THE LARGEST OF THREE NUMBERS?
~~~c
#include<stdio.h>
int main()
{
  int a,b,c;
  printf("Enter 3 numbers:");
  scanf("%d %d %d",&a,&b,&c);
  if (a>=b && a>=c)
    printf("%d is greater",a);
  else if (b>c)
    printf("%d is greater",b);
  else
    printf("%d is greater",c);
}
~~~
### Output
~~~c
Enter 3 numbers:30 10 20
30 is greater
~~~
### 8.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS A VOWEL OR CONSONANT?
~~~c
#include<stdio.h>
#include <ctype.h>
int main()
{
  char ch;
  printf("Enter a character:");
  scanf("%c",&ch);
  if(isalpha(ch))
  {
    if(ch=='a'|| ch=='A'||ch=='e'||ch=='E'||ch=='I'||ch=='i'||ch=='O'||ch=='o'||ch=='U'||ch=='u')
        printf("Vowel");
    else
        printf("Consonant");
  }
  else
    printf("Not an alphabet");
}
~~~
### Output
~~~c
Enter a character:e
Vowel
~~~
###  9.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS AN ALPHABET OR NOT
~~~c
#include<stdio.h>
int main()
{
  char ch;
  printf("Enter a character:");
  scanf("%c",&ch);
  if(ch >= 'A'&& ch <= 'Z'||ch >= 'a'&& ch <= 'z')
    printf("Alphabet");
  else
    printf("Not Alphabet");
}
~~~
### Output
~~~c
Enter a character:1
Not Alphabet
~~~
### 10.WRITE A C PROGRAM TO FIND MINIMUM OR MAXIMUM BETWEEN TWO NUMBERS?
~~~c
#include<stdio.h>
int main()
{
    int a,b;
    printf("Enter 2 numbers:");
    scanf("%d %d",&a,&b);
    if(a>b)
        printf("%d is greater than %d",a,b);
    else
        printf("%d is greater than %d",b,a);   
}
~~~
### Output
~~~c
Enter 2 numbers:10 20
20 is greater than 10
~~~

### 11.WRITE A C PROGRAM TO ENTER WEEK NUMBER AND PRINT DAY OF WEEK
~~~c
#include <stdio.h>

int main() {
  int day;
  printf("Enter week number(1-7):");
  scanf("%d",&day);
  switch(day)
  {
      case 1:printf("Sunday");
            break;
      case 2:printf("Monday");
            break;     
      case 3:printf("Tuesday");
            break;
      case 4:printf("Wednesday");
            break;
      case 5:printf("Thursday");
            break;
      case 6:printf("Friday");
            break;
      case 7:printf("Saturday");
            break;
      default:printf("Invalid Case");
            
  }
}
~~~
### Output
~~~c
Enter week number(1-7):3
Tuesday
~~~

### 12.WRITE A C PROGRAM TO CHECK WHETHER A CHARACTER IS UPPERCASE OR LOWERCASE?
~~~c
#include <stdio.h>
#include <ctype.h>

int main() {
    char ch;
    printf("Enter character:");
    scanf("%c",&ch);
    if(ch>='A'&& ch<='Z')
        printf("Uppercase");
    else if (ch>='a' && ch<= 'z')
        printf("Lowercase");
    else
        printf("Not an alphabet");
    
}
~~~
### Output
~~~c
Enter character:A
Uppercase
~~~
###  13.WRITE A C PROGRAM TO FIND NUMBER OF DAYS IN MONTH?
~~~c
#include <stdio.h>

int main() {
    int month;
    printf("Enter month(1-12):");
    scanf("%d",&month);
    switch(month)
    {
        case 1: case 3:case 5: case 7: case 8: case 10: case 12: printf("31 days");break;
        case 2: printf("28 days"); break;
        case 4: case 6: case 9: case 11: printf("30 days"); break;
    }
  
}
~~~
### Output
~~~c
Enter month(1-12):5
31 days
~~~
### 14.WRITE A C PROGRAM TO FIND MAXIMUM BETWEEN TWO NUMBERS USING SWITCH CASE?
~~~c
#include <stdio.h>

int main() {
    int a,b;
    printf("Enter two integers:");
    scanf("%d %d",&a,&b);
    int max = a>b;
    switch(max)
    {
        case 0: printf("%d is greater",b); break;
        case 1: printf("%d is greater",a); break;
        
    }
  
}
~~~
### Output
~~~c
Enter two integers:20 10
20 is greater
~~~
###  15.WRITE A C PROGRAM TO PRINT EVEN NUMBERS BETWEEN 1 TO 20 USING A FOR LOOP?
~~~c
#include <stdio.h>

int main() {
    int i=1;
    for( i=1;i<20;i++)
    {
        if(i%2==0)
        {
            printf("%d ",i);
        }
    }
  
}
~~~
### Output
~~~c
2 4 6 8 10 12 14 16 18
~~~
###  16.WRITE A C PROGRAM TO CALCULATE THE SUM OF NUMBERS FROM 1 TO 100 USING A WHILE LOOP?
~~~c
#include <stdio.h>

int main() {
  int i=1,sum=0;
  while(i<=100)
  {
      sum=sum+i;
      i++;
  }
  printf("Sum = %d",sum);
}
~~~
### Output
~~~c
Sum = 5050
~~~
###  17.WRITE A C PROGRAM TO FIND THE FACTORIAL OF A GIVEN NUMBER USING A FOR LOOP?
~~~c
#include <stdio.h>

int main() {
  int i=1,fact=1,n;
  printf("Enter number:");
  scanf("%d",&n);
  for(i=1;i<=n;i++)
  {
      fact=fact*i;
  }
  printf("Factorial of %d = %d",n,fact);
}
~~~
### Output
~~~c
Enter number:5
Factorial of 5 = 120
~~~
###  18.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN NUMBER IS PRIME OR NOT USING A WHILE LOOP.
~~~c
#include <stdio.h>

int main() {
    int num, i = 2, count = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    // Handle numbers less than 2
    if (num <= 1) {
        printf("%d is not a prime number.\n", num);
        return 0;
    }

    // Check divisibility using while loop
    while (i <= num / 2) {
        if (num % i == 0) {
            count = 1; // not prime
            break;
        }
        i++;
    }

    if (count == 0)
        printf("%d is a prime number.\n", num);
    else
        printf("%d is not a prime number.\n", num);

    return 0;
}
~~~
### Output
~~~c
Enter a number: 406
406 is not a prime number.
~~~
### 19.WRITE A C PROGRAM TO FIND THE SUM OF DIGITS OF A NUMBER USING A WHILE LOOP?
~~~c
#include <stdio.h>

int main() {
    int num,sum=0,r=0;
    printf("Enter number:");
    scanf("%d",&num);
    while(num>0)
    {
        r=num%10;
        sum+=r;
        num/=10;
    }
    printf("Sum of digits = %d",sum);   
}
~~~
### Output
~~~c
Enter number:406
Sum of digits = 10
~~~
### 20.WRITE A C PROGRAM TO PRINT FIBONACCI SERIES UP TO N TERMS USING A FOR LOOP?
~~~c
#include <stdio.h>

int main() {
    int n, first = 0, second = 1, next, i;

    printf("Enter the number of terms: ");
    scanf("%d", &n);

    printf("Fibonacci Series up to %d terms:\n", n);

    for (i = 1; i <= n; i++) {
        printf("%d ", first);
        next = first + second;
        first = second;
        second = next;
    }

    return 0;
}
~~~
### Output
~~~c
Enter the number of terms: 5
Fibonacci Series up to 5 terms:
0 1 1 2 3
~~~
###  21.WRITE A C PROGRAM TO REVERSE A GIVEN NUMBER USING A WHILE LOOP?
~~~c
#include <stdio.h>

int main() {
    int num,r=0;
    printf("Enter number:");
    scanf("%d",&num);
    printf("Reversed number is:");
    while(num>0)
    {
        r=num%10;
        printf("%d",r);
        num/=10;
    }
       
}
~~~
### Output
~~~c
Enter number:406
Reversed number is:604
~~~
### 22.WRITE A C PROGRAM TO FIND THE LARGEST ELEMENT IN AN ARRAY USING A FOR LOOP?
~~~c
#include <stdio.h>

int main() {
    int arr[50],size,large;
    printf("Enter size of array: ");
    scanf("%d",&size);
    printf("Enter array elements: ");
    for(int i=0;i<size;i++)
    {
        scanf("%d",&arr[i]);
    }
    large=arr[0];
    for(int i=1;i<size;i++)
    {
        if(arr[i]>large)
        {
            large=arr[i];
        }
    }
    printf("Largest element in the array is: %d",large);
       
}
~~~
### Output
~~~c
Enter size of array: 5
Enter array elements: 10 20 30 40 50
Largest element in the array is: 50
~~~
###  23.WRITE A C PROGRAM TO FIND THE SMALLEST ELEMENT IN AN ARRAY USING A WHILE LOOP?
~~~c
#include <stdio.h>

int main() {
    int arr[50],size,small;
    printf("Enter size of array: ");
    scanf("%d",&size);
    printf("Enter array elements: ");
    for(int i=0;i<size;i++)
    {
        scanf("%d",&arr[i]);
    }
    small=arr[0];
    int i=1;
    while(i<size)
    {
        if(arr[i]<small)
        {
            small=arr[i];
        }
        i++;
    }
    printf("Smallest element in the array is: %d",small);
       
}
~~~
### Output
~~~c
Enter size of array: 5
Enter array elements: 50 30 20 10 40
Smallest element in the array is: 10

~~~
### 24.WRITE A C PROGRAM TO PRINT ALL THE ELEMENTS OF AN ARRAY USING A FOR LOOP?
~~~c
#include <stdio.h>

int main() {
    int arr[50],size;
    printf("Enter size of array: ");
    scanf("%d",&size);
    printf("Enter array elements: ");
    for(int i=0;i<size;i++)
    {
        scanf("%d",&arr[i]);
    }
    printf("Array Elements are:");
    for(int i=0;i<size;i++)
    {
        printf("%d ",arr[i]);
    }
    
       
}
~~~
### Output
~~~c
Enter size of array: 5
Enter array elements: 1 2 3 4 5
Array Elements are:1 2 3 4 5 
~~~
###  25.WRITE A C PROGRAM TO FIND THE SUM OF ELEMENTS IN AN ARRAY USING A WHILE LOOP?
~~~c
#include <stdio.h>

int main() {
    int arr[50],size,sum=0;
    printf("Enter size of array: ");
    scanf("%d",&size);
    printf("Enter array elements: ");
    for(int i=0;i<size;i++)
    {
        scanf("%d",&arr[i]);
    }
    int i=0;
    while(i<size)
    {
      sum+=arr[i];
      i++;
    }
    printf("Sum of elements in the array is %d ",sum);
       
}
~~~
### Output
~~~c
Enter size of array: 5
Enter array elements: 1 2 3 4 5
Sum of elements in the array is 15
~~~
### 26.WRITE A C PROGRAM TO COUNT THE NUMBER OF VOWELS IN A GIVEN STRING USING A FOR LOOP?

 
 ### 27.WRITE A C PROGRAM TO COUNT THE NUMBER OF WORDS IN A GIVEN STRING USING A WHILE LOOP?
 
 ### 28.WRITE A C PROGRAM TO CHECK WHETHER A GIVEN STRING IS A PALINDROME OR NOT USING A FOR LOOP?
 
 ### 29.WRITE A C PROGRAM TO CONCATENATE TWO STRINGS WITHOUT USING LIBRARY FUNCTIONS USING A WHILE LOOP?
 
 ### 30.WRITE A C PROGRAM TO FIND THE LENGTH OF A STRING USING A FOR LOOP?
 ~~~c
#include <stdio.h>

int main() {
    char str[20];
    printf("Enter string:");
    scanf("%s",str);
    int len=0;
    for( int i=0;str[i]!='\0';i++)  
        len++;
    printf("Length of string is %d",len);
       
}
~~~
### Output
~~~c
Enter string:Github
Length of string is 6
~~~
