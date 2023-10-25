package numbergame;
import java.util.Random;
import java.util.Scanner;

public class Gameplay

{
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner reader = new Scanner (System.in);
		String Play = "yes";
		// while loop 
		
		while(Play.equals("yes"))
			{
			Random rand = new Random();
			int randNum =  rand.nextInt(100);
			
			int guess = -1;
			int tries = 0;
			
			while(guess != randNum)
			{
				System.out.println("Guess a Number Between 1 to 100");
				guess = reader.nextInt();
				tries++;
				
				if(guess == randNum)
				{
					System.out.println("Awesome You Guess The Number");
					System.out.println("It Only took you  " +tries+ "  guess!");
					System.out.println("Would you like to play again? Yes or No");
					Play = reader.next().toLowerCase();
					
				}
				else if (guess > randNum)
				{
					System.out.println("Your Guess is to high,Try again");
				}
				else
				{
					System.out.println("your Guess is to low,Try again");
				}
			}
		}
			reader.close();
	 }
	}


