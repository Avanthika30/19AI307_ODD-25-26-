# Ex.No:3(E) INNER CLASS

## QUESTION:
 Write a Java program where the inner class is declared private and accessed through a method in the outer class. 

## AIM:
To write a Java program where a private inner class is declared inside an outer class and accessed through a public method of the outer class.

## ALGORITHM :
1.	Start the program.
2.	Create an outer class with a private inner class.
3.	Declare a method inside the private inner class to display a message.
4.	Provide a public method in the outer class that creates an object of the private inner class and invokes its method.
5.	In the main method, create an outer class object and call the public method to access the private inner class.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
class data{
    private class inside{
        void display(int n)
        {
            System.out.println("Data set inside private inner class: "+n);
        }
    }
    void accessinner(int n)
    {
        inside obj=new inside();
        obj.display(n);
    }
}
public class prog{
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        data d=new data();
        int n= in.nextInt();
        d.accessinner(n);
    }
}
```
## OUTPUT:
<img width="961" height="341" alt="image" src="https://github.com/user-attachments/assets/446d3f4e-3d69-4647-ac92-e5436b2cda43" />



## RESULT:
The program successfully demonstrates how a private inner class can be accessed indirectly through a public method of the outer class.

