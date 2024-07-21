# Guessgame
// Task 1 - Guess The Number Best :

import java.util.Scanner ;
import java.util.Random ;

public class guessNumber {
    
    public static void main(String[] args) {
      Scanner sc = new Scanner(System.in) ;
      Random random = new Random(); 
      int rounds = 0 ;
      int totalAttempts = 0 ;
      boolean playAgain  = true; 
      
       System.out.print("Welcome in MJ Guess Game !:") ;
       
       while(playAgain){ 
        System.out.println("\nRounds " + rounds) ;
        rounds  ++ ;         
        int Guess = random.nextInt(100) + 1 ;
        int attempts = 0 ;
        int maxAttempts = 10 ;
        
          
        System.out.println("Enter your Guess :") ; 
        
        while(attempts < maxAttempts){
            int userNum = sc.nextInt(); 
            attempts ++ ;
            totalAttempts ++ ;
            
            
            if(userNum < Guess){
                System.out.println("Your Guess number is too small") ;
              
            }else if(userNum > Guess){
                System.out.println("Your Guess Number is too large") ;
            }else {
                System.out.println("Congratulations! you win with GuessNumber is " + Guess + " with total Attempts is " + totalAttempts);
                break ;
            }
        }
            if(attempts >=  maxAttempts) {
            
            System.out.println("Sorry you used all the attempts you are lost your Guess nuMber is  "  +Guess+ " and total Attempts are " + totalAttempts + ".") ;
            }
        
       
        
        System.out.println("You should have play another round choose (yes/No )? ") ;
        sc.nextLine() ; 
        // for nextLine Input take  ;
        // If press Yes or NO to read this take string and remove all charcters if enter user whitelspaces and case-sensitive .
        
        
        String playAgainInput = sc.nextLine().trim().toLowerCase() ;
       if(!playAgainInput.equals("yes") && !playAgainInput.equals("y")){
           playAgain = false; // stop outer loop condition :
       }
       }
    
       
       System.out.println("You have total Attemps " + totalAttempts + " and totalRounds " + rounds  +".");
       System.out.println("Thank you for playing Guess game .") ; 
        
    }
      
    }
