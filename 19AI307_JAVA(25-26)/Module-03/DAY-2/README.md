# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a class MaxFinder with three overloaded max() methods:

max(int a, int b) – returns the maximum of two integers.

max(double a, double b) – returns the maximum of two double values.

max(int a, int b, int c) – returns the maximum of three integers.

In the main() method, demonstrate the use of each overloaded method with various inputs.

## AIM:
To write a Java program that demonstrates method overloading using three max() methods that return the maximum of two integers, two doubles, and three integers.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class MaxFinder with three overloaded max() methods.
4.	Each method should return the maximum based on the number and type of parameters.
5.	In the main method, create an object of MaxFinder and call all overloaded methods with sample inputs.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
class maxfinder{
    int max(int a,int b)
    {
        return((a>b)?a:b);
    }
    double max(double a,double b)
    {
        return((a>b)?a:b);
    }
    int max(int a,int b,int c)
    {
        return((a>b&&a>c)?a:(b>c)?b:c);
    }
}
class prog{
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        maxfinder m=new maxfinder();
        int a,b;
        a=in.nextInt();
        b=in.nextInt();
        System.out.println("Max("+a+", "+b+"): "+m.max(a,b));
        double x,y;
        x=in.nextDouble();
        y=in.nextDouble();
        System.out.println("Max("+x+", "+y+"): "+m.max(x,y));
        int p,q,r;
        p=in.nextInt();
        q=in.nextInt();
        r=in.nextInt();
        System.out.println("Max("+p+", "+q+", "+r+"): "+m.max(p,q,r));
    }
}
```
## OUTPUT:
<img width="781" height="513" alt="image" src="https://github.com/user-attachments/assets/93d0e87f-14eb-46dc-a6ee-d7351ad3b911" />



## RESULT:
The program successfully demonstrates method overloading by calling different max() methods depending on the parameter list and displays the correct maximum values.
