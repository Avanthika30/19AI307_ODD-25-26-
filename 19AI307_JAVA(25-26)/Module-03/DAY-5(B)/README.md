# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To write a Java program that converts a string to an integer using a wrapper class and performs addition.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read a numeric string from the user.
4.	Convert the string to an integer using the Integer wrapper class (Integer.parseInt()).
5.	Add the integer to another number and display the result.
## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039  
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        String s1,s2;
        s1=in.next();
        s2=in.next();
        int n1,n2;
        n1=Integer.parseInt(s1);
        n2=Integer.parseInt(s2);
        System.out.println("Sum = "+(n1+n2));
    }
}
```

## OUTPUT:
<img width="433" height="426" alt="image" src="https://github.com/user-attachments/assets/a0d6bc02-4e11-440f-9db6-347ad3b21db4" />



## RESULT:
The program successfully converts a string into an integer using the Integer wrapper class and performs addition, displaying the correct final result.
