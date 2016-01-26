# Chapter4
```Java
import java.util.Scanner;
import java.io.*;

public class DistanceTravelled {

    public static void main(String[] args) {
        // Basic i/o
        System.out.print("Enter vehicle speed (in mph):");
        Scanner keyboard = new Scanner(System.in);
        String userInput = keyboard.nextLine();
        int vehicleSpeed = Integer.parseInt(userInput);
		while (vehicleSpeed < 0) {
			System.out.print(" Enter vehicle speed (in mph):");
			userInput = keyboard.nextLine();
			vehicleSpeed = Integer.parseInt(userInput);
		}
		if (vehicleSpeed >= 0){
			System.out.print(" Enter time travelled (in hrs):");
			String userInput1 = keyboard.nextLine();
			int timeTravelled = Integer.parseInt(userInput1);
			
			while (timeTravelled < 1) {
				System.out.print(" Enter time travelled (in hrs):");
				userInput1 = keyboard.nextLine();
				timeTravelled = Integer.parseInt(userInput1);
			}
			
			
			
			if (timeTravelled >= 1){
				System.out.println(" Hour"+"\t"+ "Distance Travelled");
				System.out.println("--------------------------");
				for(int i = 1; i <= timeTravelled; i++){
					System.out.println(i + "\t"+"\t" + i*vehicleSpeed);
				}
			}
			
		}
    }
}
```

```Java
import java.util.Scanner;
import java.io.*;

public class FileLetterCounter {

    public static void main(String[] args) throws IOException {
        // Basic i/o
        System.out.print("Enter file name:");
        Scanner keyboard = new Scanner(System.in);
        String fileName = keyboard.nextLine();
		System.out.print(" Enter character to count:");
		String charToCount = keyboard.nextLine();
		
		File file = new File(fileName);
		Scanner fileInput = new Scanner(file);
		
		char character = charToCount.charAt(0);
		String line;
		int count = 0;
		
		while(fileInput.hasNext()){
			line = fileInput.nextLine();
			for(int j=0; j<line.length(); j++){
				if(line.charAt(j)==character){
					count += 1;
				}
			}
		}
		
		System.out.println(" The character '" + character + "' appears in the file " + fileName +" "+ count + " times.");
		fileInput.close();
    }
}
```

```Java
import java.util.Scanner;

public class Population
{
   public static void main(String[] args){
   double organism;
   int days;
   double increase;
   Scanner input = new Scanner(System.in);
   System.out.print("Enter the starting number organisms: ");
   organism =  input.nextDouble();
   while(organism < 2){
       System.out.print("Invalid. Must be at least 2. Re-enter: ");
        organism =  input.nextDouble();
    }
   System.out.print("Enter the daily increase: ");
   increase = input.nextDouble();
   while(increase < 0){
       System.out.print("Invalid. Enter a non-negative number: ");
        increase = input.nextDouble();
    }
   System.out.print("Enter the number of days the organisms will multiply: ");
   days = input.nextInt();
   while(days < 1){
       System.out.print("Invalid. Enter 1 or more: ");
        days = input.nextInt();
    }
    System.out.println("Day\t\tOrganisms");
           System.out.println("-----------------------------");
           System.out.println("1"+ "\t\t" +organism);
           for( int i = 2; i <= days; i++){
               organism += organism*increase;
               System.out.print(i+"\t\t"+organism);
               System.out.println();
    }
}
}
```

```Java
import java.util.Scanner;

public class LargestAndSmallest {

    public static void main(String[] args){
        // Basic i/o
		Scanner keyboard = new Scanner(System.in);
		int max;
		int min;
        System.out.print("Enter an integer (-99 to stop):");
        int input = keyboard.nextInt();
		max = input;
		min = input;
		while(true){
			System.out.print(" Enter an integer (-99 to stop):");
        	input = keyboard.nextInt();
			if(input == -99){break;}
			else if(input > max){max = input;}
			else if(input < min){min = input;}
		}
		System.out.println(" The smallest number was:" + min);
		System.out.println("The largest number was: " + max);
    }
}
```

```Java
import java.util.Scanner;
public class SquareDisplay{
	public static void main(String[] args){
		// Create a Scanner object for keyboard input.
		Scanner keyboard = new Scanner(System.in);
		System.out.print("Enter an integer in the range of 1-15: ");
		// Get a number from the user.System.out.print("Enter a number between 1-15: ");
		int number = keyboard.nextInt();
		// Validate the input
		
		// display square made of char
		for (int row = 0; row < number; row++){// display row
			for (int column = 0; column < number; column++){
				char letter;
				letter = 'X';
				System.out.print(letter);
			}
			// Advance to the next line.
			System.out.println();
		}
	}
}
```
