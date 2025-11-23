# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Behavioral Design Pattern where an Article saves multiple versions of its content, stores them as mementos, allows the user to view history, and restore any previous version.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Memento class to store the article’s content as a saved version.
4.	Create an Article (Originator) class that can set content, save content into a memento, and restore content from a memento.
5.	Create a History (Caretaker) class to maintain a list of all saved mementos.
6.	In the main method, create objects for Article and History.
7.	Display a menu to the user with options to edit, save, view, and restore versions.
8.	If the user edits content, update the article.
9.	If the user chooses to save, create a memento and store it in the history list.
10.	If the user chooses to view versions, display all saved versions.
11.	If the user chooses to restore, get the selected version and restore it in the article.
12.	Continue until the user selects Exit.
13.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: AVANTHIKA.B
RegisterNumber: 212224040039 
*/
```

## SOURCE CODE:
```
import java.util.*;

class Article {
    // TODO: String content
    private String content;
    // TODO: setContent(), getContent()
    void setContent(String content)
    {
        this.content=content;
    }
    public String getContent()
    {
        return content;
    }
    // TODO: save() → returns ArticleMemento
    public ArticleMemento save()
    {
        return new ArticleMemento(content);
    }
    // TODO: restore(ArticleMemento)
    public void restore(ArticleMemento memento)
    {
        this.content=memento.getContent();
    }
}

class ArticleMemento {
    // TODO: final String content + constructor + getter
    private final String content;
    
    public ArticleMemento(String content)
    {
        this.content=content;
    }
    public String getContent()
    {
        return content;
    }
}

class ArticleHistory {
    // TODO: List to hold ArticleMemento versions
    List<ArticleMemento> versions=new ArrayList<>();
    // saveVersion(Article article)
    public void saveVersion(Article article)
    {
        versions.add(article.save());
    }
    // getVersion(int index)
    public ArticleMemento getVersion(int index)
    {
        if(index>=0 && index<versions.size())
        {
            return versions.get(index);
        }
        else
        {
            return null;
        }
    }
    // getAllVersions()
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history=new ArticleHistory();
        int n=Integer.parseInt(in.nextLine());
        
        // TODO: Read number of versions to add
        for(int i=0;i<n;i++)
        {
            String content=in.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }
        // TODO: Read and save each version
        // TODO: Read version index to restore
        int r=Integer.parseInt(in.nextLine());
        // TODO: Print restored content
        ArticleMemento m=history.getVersion(r);
        if(m!=null)
        {
            article.restore(m);
            System.out.println(article.getContent());
        }
        else
        {
        System.out.println("Invalid version");
        }

        in.close();
    }
}

```
## OUTPUT:
<img width="796" height="539" alt="image" src="https://github.com/user-attachments/assets/fadf591a-0d0b-42ab-b625-3aeee64ace0e" />



## RESULT:
The program successfully implements the Memento Behavioral Pattern, allowing an article to:

✔ Save multiple content versions
✔ Display saved versions
✔ Restore any selected version
