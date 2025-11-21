# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a java program to find the index of the last occurrence of a character in a string.

## AIM:
To write a Java program to find the index of the last occurrence of a character in a given string.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the character whose last occurrence has to be found.
4.	Use the lastIndexOf() method to find the index of the character in the string.
5.	Display the index and end the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039
*/
```

## SOURCE CODE:
```
import java.util.*;
public class jj{
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        String str=in.next();
        char letter=in.next().charAt(0);
        int last = str.lastIndexOf(letter);
        if(last !=-1)
        System.out.println("Last occurrence of '" + letter + "' is at index: " + last);
        
    }
}
```
## OUTPUT:
<img width="931" height="326" alt="image" src="https://github.com/user-attachments/assets/2438899e-527d-4e08-a1e4-e9a734003edd" />

## RESULT:
Thus, the Java program successfully finds and displays the index of the last occurrence of a character in a string.
