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
