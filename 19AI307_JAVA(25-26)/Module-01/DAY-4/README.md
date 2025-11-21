# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the sum of even and odd elements in an array

## AIM:
To write a Java program to find the sum of even and odd elements in an array.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Initialize two variables: evenSum = 0 and oddSum = 0.
4.	Traverse the array using a loop and add each element to its respective sum based on whether it is even or odd.
5.	Print the sum of even elements and the sum of odd elements, then end the program.

## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class odd{
    public static void main(String args[])
    {
        int n,i,c=0,o=0;
        Scanner in = new Scanner(System.in);
        n=in.nextInt();
        int a[]=new int[n];
        for(i=0;i<n;i++)
        {
            a[i]=in.nextInt();
            if(a[i]%2==0)
            c=c+a[i];
            else
            o=o+a[i];
        }
        System.out.println("Sum of even elements: " + c);
        System.out.println("Sum of odd elements: " + o);
    }
}
```

## OUTPUT:
<img width="809" height="689" alt="image" src="https://github.com/user-attachments/assets/becdcd97-c422-4cc5-a849-3c3cc953bfeb" />



## RESULT:
Thus, the Java program successfully calculates and displays the sum of even and odd elements in an array.
