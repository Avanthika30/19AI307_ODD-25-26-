# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:
To write a Java program that demonstrates chaining of streams by placing a BufferedReader on top of an InputStreamReader, which is built over System.in, and read input from the user.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package java.io.
3.	Create an InputStreamReader object using System.in as input source.
4.	Wrap the InputStreamReader inside a BufferedReader to enable efficient reading.
5.	Display a message asking the user to enter a string.
6.	Use the readLine() method of BufferedReader to read the input.
7.	Print the entered string back to the user.
8.	End the program.
	
## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039  
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        // Chaining: System.in -> InputStreamReader -> BufferedReader
        BufferedReader bf=new BufferedReader(new InputStreamReader(System.in));
        try{
        String name=bf.readLine();
        String n = bf.readLine();
        System.out.println("--- User Details ---");
        System.out.println("Name: "+name);
        System.out.println("Age: "+n);
        }
        catch(Exception e)
        {
            System.out.println("Error: "+e.getMessage());
        }

    }
}

```
## OUTPUT:
<img width="607" height="313" alt="image" src="https://github.com/user-attachments/assets/99def8f7-63e2-4301-a97e-2827b67bada6" />



## RESULT:
The program successfully demonstrates stream chaining by combining System.in, InputStreamReader, and BufferedReader to read a line of text from the user.
