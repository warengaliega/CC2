import java.util.Random;
public class JavaApplication26 {

    public static void main(String[] args) {
        //repetition
        //1. iteration(loops) <-- Bubble Sort
        //2. Recursion <-- Merge Sort
        //Req'd: Source Code -> Java
        //       Tests
        //       |->1 up to 100
        //       |->100 down to 1
        //       |->100 random numbers
        //Due date: Sept. 25, 2018        
        java.util.Scanner sc = new java.util.Scanner(System.in);
        System.out.println("[1] 1 up to 100");                
        System.out.println("[2] 100 down to 1");
        System.out.println("[3] 1 to 100 in random order");   
        System.out.print("Enter a number: ");
        int pagpili = sc.nextInt();               
                        
        if (pagpili == 1){
        System.out.println("1 up to 100");
        for (int i=1; i<101; i++) {
            System.out.print(i+" ");            
        }
        }
        else if (pagpili == 2){
        System.out.println("\n"
                + "\n100 down to 1");
        for (int i=100; i>=1 ; i--){
            System.out.print(i+" ");
        }
        }
        else if (pagpili == 3){
        Random rand = new Random();
        System.out.println("\n"
                + "\n100 random numbers");
        for (int i=1; i<101; i++) {
            int Random = (int)(Math.random()*100);
            System.out.print(Random+" ");
        }
        }        
    }    
}
