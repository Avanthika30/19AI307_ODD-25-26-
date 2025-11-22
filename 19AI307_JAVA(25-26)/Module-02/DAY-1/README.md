# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Course with attributes code, title, credits.

## AIM:
To write a Java program that defines a class Course with the attributes code, title, and credits, and to create an object to display the course details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define the class Course with attributes code, title, and credits.
4.	Create a constructor and a display method to show course details.
5.	In the main method, create a Course object and call the display method.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class Course {
    String code;
    String title;
    int credits;

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Course c1=new Course();
        c1.code = sc.next();
        c1.title = sc.next();
        c1.credits = sc.nextInt();

        Course c2 = new Course();
        c2.code = sc.next();
        c2.title = sc.next();
        c2.credits = sc.nextInt();

        System.out.println(c1.code + " | " + c1.title + " | " + c1.credits + " credits");
        System.out.println(c2.code + " | " + c2.title + " | " + c2.credits + " credits");

        sc.close();
    }
}

```

## OUTPUT:
<img width="854" height="331" alt="image" src="https://github.com/user-attachments/assets/4ea897d0-754b-487f-8a09-d845000113bd" />



## RESULT:
The program successfully creates a Course class with attributes code, title, and credits, and displays the details of a course using a class object.
