# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that creates a class Person with private instance variables name, age, and country, and provides public getter and setter methods to access and modify them.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Person with private variables name, age, and country.
4.	Write public getter and setter methods to access and modify these variables.
5.	In the main method, create a Person object, set values, and display them.
## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
class Person {
  
    private String name;
    private int age;
    private String country;

   
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    
    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }

    
    public String getCountry() {
        return country;
    }
    public void setCountry(String country) {
        this.country = country;
    }
}
class prog{
    public static void main(String[] args)
    {
        Scanner in = new Scanner(System.in);
        String n=in.next();
        int m=in.nextInt();
        String c=in.next();
        Person p = new Person();
        p.setName(n);
        p.setAge(m);
        p.setCountry(c);
        System.out.println("Person 1");
        System.out.println("Name: "+p.getName());
        System.out.println("Age: "+p.getAge());
        System.out.println("Country: "+p.getCountry());
    }
}
```
## OUTPUT:
<img width="779" height="542" alt="image" src="https://github.com/user-attachments/assets/c1b1a99a-1c08-44ce-a5c2-ac91dc228c8a" />



## RESULT:
The program successfully implements a Person class with private variables and public getter/setter methods and displays the values through the main method.
