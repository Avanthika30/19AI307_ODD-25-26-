# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To develop a Java program that uses the Abstract Factory Pattern to create UI components (Button and Checkbox) for two different themes: Dark and Light.
The user selects the theme at runtime, after which the appropriate factory creates the matching UI components and displays their types.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create product interfaces Button and Checkbox that define the methods for UI components.
4.	Implement concrete classes for Dark theme (DarkButton, DarkCheckbox) and Light theme (LightButton, LightCheckbox).
5.	Create an abstract factory interface UIFactory that declares methods to create the Button and Checkbox.
6.	Implement two concrete factories: DarkFactory and LightFactory, each creating theme-specific components.
7.	In the main() method, ask the user to choose a theme (1 for Dark, 2 for Light).
8.	Based on the user’s choice, create either a DarkFactory or a LightFactory instance.
9.	Use the selected factory to create a Button and Checkbox.
10.	Display the type of created UI components using their methods.
11.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;

// Product interfaces
interface Button { void create(); }
interface Checkbox { void create(); }

// Dark theme products
class DarkButton implements Button {
    public void create() { System.out.println("Dark Button created"); }
}
class DarkCheckbox implements Checkbox {
    public void create() { System.out.println("Dark Checkbox created"); }
}

// Light theme products
class LightButton implements Button {
    public void create() { System.out.println("Light Button created"); }
}
class LightCheckbox implements Checkbox {
    public void create() { System.out.println("Light Checkbox created"); }
}

// Abstract factory
interface GUIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// Concrete factories
class DarkFactory implements GUIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}
class LightFactory implements GUIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

// Main class
public class UIFactoryDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine().trim().toLowerCase();
        GUIFactory factory = null;

        if (theme.equals("dark")) factory = new DarkFactory();
        else if (theme.equals("light")) factory = new LightFactory();
        else {
            System.out.println("Invalid theme" );
            return;
        }

        factory.createButton().create();
        factory.createCheckbox().create();
    }
}

```
## OUTPUT:
<img width="671" height="303" alt="image" src="https://github.com/user-attachments/assets/df9ebe4f-2c00-4b4e-b5c4-5fcca2e54e2b" />



## RESULT:
The program successfully demonstrates the Abstract Factory Pattern by allowing the user to choose a UI theme at runtime.
Based on the selected theme, the appropriate factory creates and displays the corresponding Button and Checkbox components (Dark or Light).

✔ Dark theme creates: Dark Theme Button, Dark Theme Checkbox
✔ Light theme creates: Light Theme Button, Light Theme Checkbox
