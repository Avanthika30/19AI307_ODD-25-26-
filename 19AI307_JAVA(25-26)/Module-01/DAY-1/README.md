# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely finds an ancient vault secured by binary locks. Each lock responds to bitwise operations to determine whether it opens or stays shut.

To unlock the vault, she is given two integers that represent key codes in binary. 

She needs to apply these operations and report the results.

## AIM:
To write a Java program that accepts two integer key codes and performs bitwise operations—AND, OR, XOR, left shift of the first key, and right shift of the second key—and displays the results in the specified format to simulate the unlocking mechanism of an ancient vault.

## ALGORITHM :

1.	Start and read two integer inputs representing the key codes.
2.	Apply bitwise AND operation on the two keys and store the result.
3.	Apply bitwise OR and bitwise XOR operations on the two keys and store their results.
4.	Left shift the first key by 1 bit and right shift the second key by 1 bit.
5.	Display all the results in the required output format.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## Sourcecode.java:
```
import java.util.*;
class prog{
    public static void main(String args[])
    {
        int a,b;
        Scanner in = new Scanner(System.in);
        a=in.nextInt();
        b=in.nextInt();
        
        System.out.println("Bitwise AND: "+(a&b));
        System.out.println("Bitwise OR: "+(a|b));
        System.out.println("Bitwise XOR: "+(a^b));
        System.out.println("First Key << 1: "+(a<<1));
        System.out.println("Second Key >> 1: "+ (b>>1));
    }
}
```
## OUTPUT:
<img width="601" height="339" alt="image" src="https://github.com/user-attachments/assets/d10636b4-9428-466a-8460-8ab768c407d0" />



## RESULT:
Thus,the bitwise operation results for the two given keys were displayed successfully.

