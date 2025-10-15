 1.WRITE A C PROGRAM TO ACCEPT TWO INTEGERS AND CHECK WHETHER THEY ARE EQUAL OR 
NOT?
~~~~c
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
```
### Output
~~~c
enter 2 integers:2 3
Both are not equal.
~~~
