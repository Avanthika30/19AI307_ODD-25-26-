# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to print the Fibonacci series using a for loop. The series starts with 0 and 1, and the next number is the sum of the previous two.

## AIM:
To write a Java program that prints the Fibonacci series using a for loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read the number of Fibonacci terms from the user.
4.	Initialize the first two Fibonacci numbers (a = 0, b = 1) and print them.
5.	Use a for loop to calculate and print the remaining Fibonacci numbers by adding the previous two.
6.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class fib{
    public static void main(String args[])
    {
        int n,a,b;
        Scanner in = new Scanner(System.in);
        n=in.nextInt();
        a=0;
        b=1;
        System.out.printf("Fibonacci Series: %d %d ",a,b);
        for(int i=3;i<=n;i++)
        {
            int temp=a+b;
            a=b;
            b=temp;
            System.out.printf("%d ",temp);
        }
    }
}
```
## OUTPUT:
<img width="826" height="336" alt="image" src="https://github.com/user-attachments/assets/0f2d4a44-71a5-4a62-9632-5ddcd96d8371" />



## RESULT:
Thus, the Java program successfully prints the Fibonacci series using a for loop.
