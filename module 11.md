

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:

```
#include<stdio.h>
int max(int x, int y)
{
    return (x>y)?x:y;
}
int max_of_four(int a, int b, int c, int d)
{
    return max(max(a,b),max(c,d));  
}
int main(){
    int a,b,c,d;
    scanf("%d%d%d%d",&a,&b,&c,&d);
    printf("%d",max_of_four(a,b,c,d));
}
```

Output:

<img width="1261" height="358" alt="image" src="https://github.com/user-attachments/assets/0c937d04-496c-4999-b489-a795b1a77c80" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:

```
#include<stdio.h>

void calculate_the_maximum(int x,int y){
    int max_and =0,max_or=0,max_xor=0;
    
    for(int i=1;i<=x;i++){
        for(int j=i+1;j<=x;j++){
            int andv =i&j;
            int orv=i|j;
            int xorv=i^j;
            
            
            if(andv < y && max_and < andv) max_and=andv;
            if(orv < y && max_or < orv) max_or=orv;
            if(xorv < y && max_xor <xorv) max_xor=xorv;
        }
    }
    printf("%d\n%d\n%d",max_and,max_or,max_xor);
}
int main(){
    int a,b;
    scanf("%d%d",&a,&b);
    calculate_the_maximum(a,b);
    return 0;
}
```

Output:

<img width="1261" height="383" alt="image" src="https://github.com/user-attachments/assets/9a7f7afc-0e3b-4d72-a004-d78b6340474a" />


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:

```
#include<stdio.h>
#include<stdlib.h>

int main(){
    
    int t,q;
    scanf("%d%d",&t,&q);
    
    int **s=(int **)malloc(t*sizeof(int *));
    int *bc=(int *)malloc(t*sizeof(int));
    
    for(int i=0;i<t;i++){
        s[i]=NULL;
        bc[i]=0;
    }
    
    for(int i=0;i<q;i++){
        int que;
        scanf("%d",&que);
        
        if(que==1){
            int x,y;
            scanf("%d%d",&x,&y);
            
            s[x]=(int *)realloc(s[x],(bc[x]+1)*sizeof(int));
            s[x][bc[x]]=y;
            bc[x]++;
        }   
            
        if(que==2){
            int x,y;
            scanf("%d%d",&x,&y);
            printf("%d\n",s[x][y]);
        }
        
        if(que==3){
            int x;
            scanf("%d",&x);
            printf("%d\n",bc[x]);
        }
    }
    for(int i=0;i<t;i++){
        free(s[i]);
    }
    
    free(s);
    free(bc);
}
```

Output:

<img width="1271" height="279" alt="image" src="https://github.com/user-attachments/assets/f43c9744-b814-49b1-b809-cb8a2d907b07" />



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:

```
#include<stdio.h>

void TOTDET(int a,int b,int c,int d,int e){
    
    float tot=a+b+c+d+e;
    float avg=tot/5;
    float per=(tot*100)/500;
    
    printf("%.6f\n%.6f\n%.6f",tot,avg,per);
}
int main(){
    int a,b,c,d,e;
    scanf("%d%d%d%d%d",&a,&b,&c,&d,&e);
    TOTDET(a,b,c,d,e);
}
```

Output:

<img width="1266" height="263" alt="image" src="https://github.com/user-attachments/assets/0691553c-22b3-4116-95a3-295e3b8a6144" />


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:

```
#include <stdio.h>
#include <string.h>

int main() {
    char str[200];
    int count = 0, i;

    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++) {
        if ((i == 0 && str[i] != ' ') || 
            (str[i] != ' ' && str[i-1] == ' ')) {
            count++;
        }
    }

    printf("Number of words: %d\n", count);
    return 0;
}

```

Output:

<img width="1665" height="675" alt="image" src="https://github.com/user-attachments/assets/96f6a7f3-9b31-4dbd-959a-9ab7812e53a9" />






Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
