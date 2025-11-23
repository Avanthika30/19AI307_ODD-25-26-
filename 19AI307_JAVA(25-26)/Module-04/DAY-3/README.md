# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
A student can enroll in multiple courses. The relationship is many-to-many via association.
If No Courses were assigned, print "No courses enrolled." 

## AIM:
To write a Java program that demonstrates a many-to-many association between students and courses, where a student can enroll in multiple courses.
If no courses are assigned, the program must display “No courses enrolled.”

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Course class with an attribute to store the course name.
4.	Create a Student class containing the student name and a list to store multiple course objects.
5.	Define a method enroll() in the student class that adds a course to the student's course list.
6.	Define a method showCourses() that:
         Checks if the list of courses is empty.
         If empty, prints “No courses enrolled.”
         Otherwise, prints all enrolled course names.
7.In the main() method, read the number of courses to be assigned to the student.
8.If the number of courses is zero, directly display “No courses enrolled.”
9.Otherwise, read each course name, create a Course object, and enroll the student.
10.Display the enrolled courses.
11.End the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class AssociationExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String studentName = sc.nextLine();
        Student student = new Student(studentName);

        int n = sc.nextInt();
        sc.nextLine(); 

        for (int i = 0; i < n; i++) {
            String course = sc.nextLine();
            student.enroll(new Course(course));
        }

        student.showCourses();
        sc.close();
    }
}

class Course {
    private String name;

    public Course(String name) {
        this.name = name;
    }

    public String getCourseName() {
        return name;
    }
}

class Student {
    private String name;
    private List<Course> courses;

    public Student(String name) {
        this.name = name;
        this.courses = new ArrayList<>();
    }

    public void enroll(Course c) {
        courses.add(c);
    }

    public void showCourses() {
        if (courses.isEmpty()) {
            System.out.println(name + "'s enrolled courses:");
            System.out.println("No courses enrolled.");
        } else {
            System.out.println(name + "'s enrolled courses:");
            for (Course c : courses) {
                System.out.println("- " + c.getCourseName());
            }
        }
    }
}

```
## OUTPUT:
<img width="937" height="381" alt="image" src="https://github.com/user-attachments/assets/4d09e6c2-5eb0-4786-96b4-bf2bcac4013d" />



## RESULT:
Thus, the program successfully demonstrates a many-to-many association between students and courses.
It correctly handles cases where a student enrolls in multiple courses and also displays “No courses enrolled.” when no courses are assigned.
