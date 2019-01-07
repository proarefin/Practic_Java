import java.lang.Math; // headers MUST be above the first class
import java.util.*;
// one class needs to have a main() method
public class HelloWorld
{
  // arguments are passed using the text field below this editor
  public static void main(String[] args)
  {
    OtherClass myObject = new OtherClass();
    System.out.print(myObject.anonymousLoveLetter("the love letter", "this is the newspaper string lol total vote"));
    System.out.print(myObject.anonymousLoveLetter("the love letter", "This is the newspaper"));
  }
}

// you can add other public classes to this editor in any order
public class OtherClass
{
  
  final Counter<String> counts = new Counter<>();
  public boolean anonymousLoveLetter(String L, String N)
  {
    char l[] = L.toCharArray();
    for(char c : l)
    {
        counts.add(Character.toString(c));
    }
    
    char n[] = N.toCharArray();
    int count=L.length();
    for(char c : n)
    {
    
      //message = Character.toString(c); 
     if(counts.count(Character.toString(c)) >= 1)
     {
       counts.remove(Character.toString(c));
       count -=1;
     }
    if(count==0)    
    	return true;
    }
    return false;
  }
}
public class Counter<T> {
    final Map<T, Integer> counts = new HashMap<>();

    public void add(T t) {
        counts.merge(t, 1, Integer::sum);
    }
    public void remove(T t) {
        counts.merge(t, -1, Integer::sum);
    }

    public int count(T t) {
        return counts.getOrDefault(t, 0);
    }
}
