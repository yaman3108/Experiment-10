# Experiment 10



## Aim:
To study and implement Pointer Operations (Call by value and Call by reference)


## Apparatus:
Vs Code, Github


## Theory:

### Call by value:
A function receives a copy of the argument's value, not the original data. Changes made within the function affect only the copy and do not alter the original data. This is less efficient for large data but is safer as the original data is not altered.

### Call by referenece:
A function receives a reference (or address) to the original argument, allowing it to modify the actual data. Changes made within the function directly affect the original variable. This is more efficient for large data but is unsafe as the original data can get altered.


## Code:

### Call by value:
```
#include<iostream>
using namespace std;
void swap(int x, int y)
{
  int swap;
  swap=x;
  x=y;
  y=swap;
}

int main() 
{
  int a=5,b=2;
  swap(a,b);
  cout<<"Value of a is: "<<a<<endl;
  cout<<"Value of b is: "<<b<<endl;
  return 0;
}
```
### Output:
![Screenshot 2024-09-02 141131](https://github.com/user-attachments/assets/99becb2d-dac1-4c6b-a444-4214aa07dc2f)

### Call by reference:
```
#include<iostream>
using namespace std;
void swap(int *x, int *y)
{
  int swap;
  swap=*x;
  *x=*y;
  *y=swap;
}

int main() 
{
  int a=10,b=20;
  swap(&a,&b);
  cout<<"Value of a is: "<<a<<endl;
  cout<<"Value of b is: "<<b<<endl;
  return 0;
}
```
### Output:
![Screenshot 2024-09-02 141343](https://github.com/user-attachments/assets/2dfc213d-79ea-4375-acfd-43db21c3dc1f)


## Conclusion:
This program helps us understand how call by value and call by reference work in C++. What differences they make during programing and how they differ in functionality.
