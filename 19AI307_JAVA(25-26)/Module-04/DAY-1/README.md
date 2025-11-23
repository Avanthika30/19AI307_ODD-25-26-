# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To write a Java program that reads a string input, checks for a null value, and converts the string to uppercase.
If the input represents a null value, the program must throw and handle a NullPointerException.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read input from the user.
4.	Read a string from the user.
5.	Check if the input string equals "null".
6.	If yes, manually throw a NullPointerException.
7.	If the string is not null, convert it to uppercase using toUpperCase() and print it.
8.	Use a try–catch block to handle the NullPointerException.
9.	If caught, display "Null element".
10.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
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
        
        try{
            
                String a=in.next();
                if(a.equals("null"))throw new NullPointerException();
                else
                System.out.println(a.toUpperCase());
            }
        
        catch(NullPointerException e)
        {
            System.out.println("Null element");
        }
    }
}
```
## OUTPUT:
<img width="609" height="353" alt="image" src="https://github.com/user-attachments/assets/72b463da-9d63-40bf-b172-52d6b32796eb" />



## RESULT:
The program successfully reads a string and prints it in uppercase.
