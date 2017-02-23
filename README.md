# EnRoute
for fun

/**
 * 
 * Calla Edwards
 */
import java.util.*;
public class EnRoute
{
    public static void main (String [] args)
    {
        Scanner console = new Scanner(System.in);
        System.out.println("Hall:");
        String walk = console.nextLine();
        int salutes=0;
        while (walk.indexOf(">") < 0 || walk.indexOf("<") < 0){
            System.out.println("Try again");
            System.out.println("Hall: ");
            walk = console.nextLine();
        }
        
        if (walk.indexOf (">") < walk.indexOf ("<")){
         for(int c=walk.indexOf(">");c>=0;c=walk.indexOf(">",c+1))
         {
                for(int d=c+1; walk.indexOf("<",d) > 0; d=walk.indexOf("<",d)+1){
                    salutes+=2;
                }
            }
         }
        
        
        System.out.printf("There were %d salutes which took %d seconds.", salutes,salutes*5);
        
    }
}
