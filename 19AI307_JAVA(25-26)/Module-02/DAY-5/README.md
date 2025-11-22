# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.

## AIM:
To write a Java program that defines a class Student with variables name and rollNumber, and uses a method setDetails() to assign values and another method to display them.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Student with variables name and rollNumber.
4.	Write a method setDetails(String name, int rollNumber) and a method to display details.
5.	In the main method, create a Student object, set details, and display them.

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Student {
    String name;
    int rollNumber;
    Student(String nam, int roll)
   {
    this.name=nam;
    this.rollNumber=roll;
   }
    void setDetails()
   {
     System.out.println("Name: "+name);
     System.out.println("Roll Number: "+rollNumber);
   }
}
class prog {
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        String nam=in.next();
        int roll=in.nextInt();
        Student s=new Student(nam,roll);
        s.setDetails();
    }
}
```

## OUTPUT:
<img width="561" height="395" alt="image" src="https://github.com/user-attachments/assets/f7fe75e4-a490-4922-a5f9-02169726d06b" />

## RESULT:
The program successfully creates a Student class, sets the details using setDetails(), and displays the values using the display method.
