# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A pirate ship has a code lock that only opens if:

The input code is even, and

If it is less than 100, say "Weak Code".

If it is between 100 and 999, say "Strong Code".

If the code is odd, deny access.

## AIM:
To classify a pirate code as Weak, Strong, or Denied.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the input code from the user.
4.	Check if the code is odd — if true, print "Access Denied".
5.	If the code is even and less than 100, print "Weak Code".
6.	If the code is even and between 100 and 999, print "Strong Code".
7.	End the program.

## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class pirate{
    
    public static void main(String arg[])
    {
        int num;
        Scanner in = new Scanner(System.in);
        num=in.nextInt();
        if(num%2==0)
        {
            if(num<100)
            System.out.println("Weak Code");
            else if(num>100 && num<999)
            System.out.println("Strong Code");
            else
            System.out.println("Access Denied");
        }
        else
         System.out.println("Access Denied");
    }
}
```
## OUTPUT:
<img width="572" height="374" alt="image" src="https://github.com/user-attachments/assets/dae2b989-f163-41dc-8624-39338702af66" />


## RESULT:
Thus, the Java program successfully checks the pirate code and displays whether it is a Weak Code, Strong Code, or Access Denied.
