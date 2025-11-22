# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that defines a method cube(int x) which internally calls the method square(int x) to compute the cube of a number.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define methods square(int x) and cube(int x) where cube calls square internally.
4.	In the main method, read a number from the user and call cube().
5.	Display the cube value and end the program.

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    int cube(int x)
    {
        return x*square(x);
    }
    int square(int x)
    {
        return x*x;
    }
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        int n=in.nextInt();
        prog p=new prog();
        System.out.println(p.cube(n));
    }
}
```
## OUTPUT:
<img width="408" height="250" alt="image" src="https://github.com/user-attachments/assets/d5400e4f-e921-4e2d-a3fe-249cb7325bf3" />



## RESULT:
The program successfully calculates the cube of a number by calling the square() method from inside the cube() method.
