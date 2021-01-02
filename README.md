package com.company;                                                                                                                                
                                                                                                                                                    
import java.util.Scanner;                                                                                                                           
                                                                                                                                                    
public class Main {                                                                                                                                 
                                                                                                                                                    
    public static void main(String[] args) {                                                                                                        
        //creates a variable computerChoice of type string                                                                                          
        String computerChoice;                                                                                                                      
        //creates integers wins and losses to keep track of score                                                                                   
        int wins = 0;                                                                                                                               
        int losses = 0;                                                                                                                             
                                                                                                                                                    
       //instructions to the user displayed on screen                                                                                               
        System.out.println("Do you choose 'r' for rock, 'p' for paper, or 's' for scissors?");                                                      
        System.out.println("**********************************************");                                                                       
        //Displays the current score: Wins and Losses                                                                                               
        System.out.print("Wins: " + wins);                                                                                                          
        System.out.println("\t Losses: " + losses);                                                                                                 
                                                                                                                                                    
        //get user input: r, p or s to play game                                                                                                    
        System.out.println("Players Choice:");                                                                                                      
                                                                                                                                                    
        //create a Scanner object                                                                                                                   
        Scanner user_Choice = new Scanner(System.in);                                                                                               
        String userChoice = user_Choice.nextLine();                                                                                                 
        //Loop starts                                                                                                                               
        do {                                                                                                                                        
            //Random number generator                                                                                                               
            double rand = Math.random() * 100;                                                                                                      
                                                                                                                                                    
            //Assigning a value of r, p or s for computerChoice depending on the random generator                                                   
            if (rand < 34) {                                                                                                                        
                computerChoice = "r";                                                                                                               
            } else if (rand < 67) {                                                                                                                 
                computerChoice = "p";                                                                                                               
            } else computerChoice = "s";                                                                                                            
                                                                                                                                                    
                                                                                                                                                    
            //If the outcome results in a Draw                                                                                                      
            if (userChoice.equals(computerChoice)) {                                                                                                
                System.out.println("Draw!");                                                                                                        
                                                                                                                                                    
            }                                                                                                                                       
            //if and else statements used to identify the winner and loser when player picks "r"/rock                                               
            if (userChoice.equals("r")) {                                                                                                           
                if (computerChoice.equals("s")) {                                                                                                   
                    System.out.println("You Win!");                                                                                                 
                    wins++;                                                                                                                         
                } else {                                                                                                                            
                    if (computerChoice.equals("p")) {                                                                                               
                        System.out.println("You Lose");                                                                                             
                        losses++;                                                                                                                   
                    }                                                                                                                               
                }                                                                                                                                   
            }                                                                                                                                       
            //if and else statements used to identify the winner and loser when player picks "p"/paper                                              
            if (userChoice.equals("p")) {                                                                                                           
                if (computerChoice.equals("r")) {                                                                                                   
                    System.out.println("You Win!");                                                                                                 
                    wins++;                                                                                                                         
                } else {                                                                                                                            
                    if (computerChoice.equals("s")) {                                                                                               
                        System.out.println("You Lose");                                                                                             
                        losses++;                                                                                                                   
                    }                                                                                                                               
                }                                                                                                                                   
            }                                                                                                                                       
            //if and else statements used to identify the winner and loser when player picks "s"/scissors                                           
            if (userChoice.equals("s")) {                                                                                                           
                if (computerChoice.equals("p")) {                                                                                                   
                    System.out.println("You Win!");                                                                                                 
                    wins++;                                                                                                                         
                } else {                                                                                                                            
                    if (computerChoice.equals("r")) {                                                                                               
                        System.out.println("You Lose");                                                                                             
                    losses++;                                                                                                                       
                    }                                                                                                                               
                }                                                                                                                                   
            }                                                                                                                                       
            //If statement used to document the computer and player choices                                                                         
            if (computerChoice.equals("r")) {                                                                                                       
                System.out.print("Computer Choice: rock");                                                                                          
            }                                                                                                                                       
            if (computerChoice.equals("p")) {                                                                                                       
                System.out.print("Computer Choice: paper");                                                                                         
            }                                                                                                                                       
            if (computerChoice.equals("s")) {                                                                                                       
                System.out.print("Computer Choice: scissors");                                                                                      
            }                                                                                                                                       
            if (userChoice.equals("r")) {                                                                                                           
                System.out.println("\t Player Choice: rock");                                                                                       
            }                                                                                                                                       
            if (userChoice.equals("p")) {                                                                                                           
                System.out.println("\t Player Choice: paper");                                                                                      
            }                                                                                                                                       
            if (userChoice.equals("s")) {                                                                                                           
                System.out.println("\t Player Choice: scissors");                                                                                   
            }                                                                                                                                       
        //print out after each loop with updated score                                                                                              
        System.out.println("**********************************************");                                                                       
        System.out.print("Wins: " + wins);                                                                                                          
        System.out.println("\t Losses: " + losses);                                                                                                 
        System.out.println("Players Choice:");                                                                                                      
        //asks user if they want to play again by selecting r,p or s                                                                                
        userChoice = user_Choice.nextLine();                                                                                                        
        //While statement to see if the user picks the right input - r,p or s - if correct then the loop starts again; if not the program ends      
        }while(userChoice.equals("r") || userChoice.equals("p") || userChoice.equals("s"));                                                         
        //Thanks user for playing                                                                                                                   
        System.out.println("Thank you for playing!");                                                                                               
    }                                                                                                                                               
}                                                                                                                                                   
                                                                                                                                                    
