# Ex.No:3(D)    INTERFACE 

## QUESTION:
Each judge uses different criteria to score fighters. Based on points, the judge will declare “WIN”, “LOSE” or “DRAW”.

LenientJudge: WIN if diff ≥ 5, DRAW if < 5

StrictJudge: WIN if diff ≥ 10, DRAW if < 10

Input Format:

player1Score
player2Score
judgeType
player1Score, player2Score: integers

judgeType: 1 for LenientJudge, 2 for StrictJudge

Output Format:
WIN / LOSE / DRAW

## AIM:
To write a Java program that determines the match result (WIN / LOSE / DRAW) using two judge types: LenientJudge and StrictJudge, based on the score difference between two fighters.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read player1Score, player2Score, and judgeType from the user.
4. Based on judgeType, use LenientJudge or StrictJudge to evaluate the result.
5. Display WIN, LOSE, or DRAW according to the scoring rules.	

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;
interface judge{
    String out(int a,int b);
}
class lenient implements judge{
    public String out(int a,int b)
    {
        int diff = Math.abs(a-b);
        if(diff>=5)
        {
        if(a>b)
        return "WIN";
        else
        return "LOSE";
        }
        else
        return "DRAW";
    }
}
class strict implements judge{
    public String out(int a,int b)
    {
        int diff = Math.abs(a-b);
        if(diff>=10)
        {
        if(a>b)
        return "WIN";
        else
        return "LOSE";
        }
        else
        return "DRAW";
    }
}
class prog{
    public static void main(String args[])
    {
        Scanner in = new Scanner(System.in);
        judge j;
        int a=in.nextInt();
        int b=in.nextInt();
        int type=in.nextInt();
        if(type==1)
        {
            j=new lenient();
            System.out.println(j.out(a,b));
        }
        else
        {
            j=new strict();
            System.out.println(j.out(a,b));
        }
    }
}
```
## OUTPUT:
<img width="445" height="409" alt="image" src="https://github.com/user-attachments/assets/1686b08b-a6af-4d84-b7cd-48031a8aa046" />



## RESULT:
The program successfully applies the scoring rules of LenientJudge and StrictJudge based on the input score difference and outputs the correct match result: WIN, LOSE, or DRAW.
