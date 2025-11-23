# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
You are designing a microservices-based system where multiple services like AuthService, UserService, OrderService, etc., need to log important system events.

To maintain centralized logging (and not have separate loggers for each service), the system uses a Singleton Logger.

Each service logs messages with its name and log level.

Log levels can be: INFO, WARNING, or ERROR.

Every log message is stored in order of occurrence and the logger prints the entire log history each time a new message is added.

🧩 Concepts Student Must Apply:
Implement a Singleton class (Logger) that holds logs.

Maintain logs as a list of strings.

Each log message must be formatted as:
"[Service] [LEVEL]: message"

Print full log history after each new log.

Input Format:
First line: Integer n – number of logs

Next n lines: Each contains:
[ServiceName] [Level] [Message]
(The message has no spaces.)

Output Format:
After each log, print:

[Service] [LEVEL]: message
Current Logs:
1. log1
2. log2
...

## AIM:
To write a Java program that implements a Singleton Logger used by multiple microservices to log system events.
The logger must store all logs in order, and after each new log entry, it should print the entire log history.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number of log entries from the user.
4.	Create or access the Singleton Logger instance.
5.	For each entry, read the service name, log level, and message.
6.	Pass these values to the logger’s addLog() method to store and display logs.
7.	Print the updated log history after every new log.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;

class Logger {
    private static Logger instance;
    private List<String> logs;

    private Logger() {
       //Type your code
       logs=new ArrayList<>();
    }

    public static Logger getInstance() {
	//Type your code
	if(instance==null)
	{
	    instance=new Logger();
	}
	return instance;
        
    }
    public void addLog(String service, String level, String message) {
        //Type your code
        String log=service + " " +level+": "+message;
        logs.add(log);
        System.out.println(log);
        System.out.println("Current Logs:");
        for(int i=0;i<logs.size();i++)
        {
            System.out.println((i+1)+". "+logs.get(i));
        }
}
}
public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); sc.nextLine();

        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ");
            String service = input[0];
            String level = input[1];
            String message = input[2];

            Logger logger = Logger.getInstance();
            logger.addLog(service, level, message);
            System.out.println();
        }
    }
}

```
## OUTPUT:
<img width="1239" height="803" alt="image" src="https://github.com/user-attachments/assets/ebb55190-48d0-4d94-a44b-b5e191da8f96" />



## RESULT:
Thus, the Java program successfully implements a Singleton Logger that:
✔ Accepts log requests from multiple microservices
✔ Stores logs in sequence
✔ Prints the entire log history after each new log entry

The program demonstrates correct usage of the Singleton design pattern and logging mechanism.
