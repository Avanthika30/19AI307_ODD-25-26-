# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to create a new file named example.txt.

## AIM:
To write a Java program that creates a new file named example.txt using Java File Handling.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package java.io.
3.	Create a File object with the filename "example.txt".
4.	Call the createNewFile() method to create the file.
5.	If the file is created successfully, print a success message.
6.	If the file already exists, print an appropriate message.
7.	Handle any possible exceptions.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.io.*;

class CreateFileDemo {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");

            if (file.createNewFile()) {
                System.out.println("File created: " + file.getName());
            } else {
                System.out.println("File already exists.");
            }
        } catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
    }
}

```
## OUTPUT:
<img width="649" height="257" alt="image" src="https://github.com/user-attachments/assets/f7c29371-ccaa-4496-8433-6172064e26ed" />



## RESULT:
The program successfully creates a new file named example.txt if it does not already exist.
