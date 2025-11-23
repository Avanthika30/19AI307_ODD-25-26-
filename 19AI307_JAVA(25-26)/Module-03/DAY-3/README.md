# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2
Second line: base, level (or attempts)

Output Format:

Final score (int)

## AIM:
To write a Java program that defines an abstract class GameScore with an abstract method finalScore(), and implements two subclasses ArcadeGame and PuzzleGame to calculate the final score based on given rules.

## ALGORITHM :
1.	Start the program.
2.	Create an abstract class GameScore with an abstract method finalScore().
3.	Create subclasses ArcadeGame and PuzzleGame implementing their own scoring formulas.
4.	Read input from the user and create the appropriate subclass object.
5.	Call finalScore() and print the result.
	
## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class gamescore{
    abstract int finalscore();
}
class arcade extends gamescore{
    int base,level;
    arcade(int b,int l)
    {
        this.base=b;
        this.level=l;
    }
    int finalscore()
    {
        return (base + (level * 100));
    }
}
class puzzle extends gamescore{
    int attempts;
    puzzle(int a)
    {
        this.attempts=a;
    }
    int finalscore()
    {
        return ((attempts <= 3) ? 1000 - (attempts * 100) : 500);
    }
}
class prog{
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        gamescore g;
        int n=in.nextInt();
        if(n==1)
        {
            int b=in.nextInt();
            int l=in.nextInt();
            g=new arcade(b,l);
            System.out.println(g.finalscore());
        }
        else
        {
            int a=in.nextInt();
            g=new puzzle(a);
            System.out.println(g.finalscore());
        }
    }
}
```
## OUTPUT:
<img width="454" height="323" alt="image" src="https://github.com/user-attachments/assets/e2cb0d31-def4-4495-8144-b3092d311efd" />



## RESULT:
The program successfully implements an abstract class GameScore and its subclasses ArcadeGame and PuzzleGame, calculates the final score based on user input, and displays the correct final score according to the defined scoring rules.
