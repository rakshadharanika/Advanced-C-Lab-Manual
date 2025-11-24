EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:
```
#include<stdio.h>
struct eligib
{
 int age;
 char n[4];
};
int main()
{
 struct eligib e;
 scanf("%d%s",&e.age,e.n);
 if(e.age<=6)
 {
 printf("Age:%d\nName:%svaccine:%d\neligibility:no",e.age,e.n,e.age);
 }
 else
 {
 printf("Age:%d\nName:%svaccine:%d\neligibility:yes",e.age,e.n,e.age);
 }
}
```

Output:

<img width="742" height="287" alt="image" src="https://github.com/user-attachments/assets/a850b93a-601f-48f5-9673-f3c4d29ee9fe" />



Result:
Thus, the program is verified successfully.
