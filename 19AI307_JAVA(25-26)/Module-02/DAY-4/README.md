# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Create a constructor in a class and call a normal method from it. 

## AIM:
To write a Java program that defines a constructor inside a class and calls a normal method from within the constructor.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with a constructor and a normal method.
4.	Call the normal method from inside the constructor.
5.	In the main method, create an object to invoke the constructor and execute the method.

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog{
    static String s;
    static int n;
    prog(String m,int x)
    {
        s=m;
        n=x;
    }
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        String m = in.next();
        int x=in.nextInt();
        prog p=new prog(m,x);
        System.out.println("Student Name: "+prog.s);
        System.out.println("Marks Scored: "+prog.n);
        if(prog.n>30)
        System.out.println("Status: Pass");
        else
        System.out.println("Status: Fail");
    }
}
```
## OUTPUT:
<img width="584" height="431" alt="image" src="https://github.com/user-attachments/assets/cf54187d-07b8-4aae-b4f4-3aa8678f35e7" />



## RESULT:
The program successfully calls a normal method from inside the constructor when the object is created.
