MainClassHangman
================
import java.util.Scanner;

public class Play {
	public static void main(String[] args) {		
		
		System.out.println("Welcome to Hangman !");
		System.out.println();
		// Choose a category here - Engin
		// Викане на моя метод chooseDifficulty();
		chooseDifficulty();	
	}

	private static void chooseDifficulty() {
		
		System.out.println("Choose a difficulty(1-3):");
		
		Scanner input = new Scanner(System.in);
		int difficulty = input.nextInt();
		
		switch (difficulty) {
		case 1:
			System.out.println("You chose difficulty 1: You have 10 tries to guess the word. "
					+ "You will also have a hint for the word that you have to guess.");
			PlayBody obj = new PlayBody();
			obj.Start(difficulty);						
			break;
		case 2:
			System.out.println("You chose difficulty 2: You have 7 tries to guess the word. "
					+ "You will also have a hint for the word that you have to guess.");
			obj = new PlayBody();
			obj.Start(difficulty);						
			break;
		case 3:
			System.out.println("You chose difficulty 3: You have 5 tries to guess the word, "
					+ "otherwise you lose.");	
			obj = new PlayBody();
			obj.Start(difficulty);					
			break;
		default:System.out.println("Invalid choice! Please input a number from 1-3 !");
			break;
		}
	}
}
