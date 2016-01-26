# Chapter 3 Java

GitBook allows you to organize your book into chapters, each chapter is stored in a separate file like this one.

```Java
import java.util.Scanner;
/**
 * @author Aaron Kolker
 * @version 1.0.0
 * Comment
 */
public class RomanNumerals {

    public static void main(String[] args) {
        //Define variables
        String userInput;
        int input;
        String romanNumeral;
        //user input
        System.out.print("Enter a number in the range of 1 - 10: ");
        Scanner keyboard = new Scanner(System.in);
        userInput = keyboard.nextLine();
        input = Integer.parseInt(userInput);
        switch (input) {
            case 1:  romanNumeral = "I";
                break;
            case 2:  romanNumeral = "II";
                break;
            case 3:  romanNumeral = "III";
                break;
            case 4:  romanNumeral = "IV";
                break;
            case 5:  romanNumeral = "V";
                break;
            case 6:  romanNumeral = "VI";
                break;
            case 7:  romanNumeral = "VII";
                break;
            case 8:  romanNumeral = "VIII";
                break;
            case 9:  romanNumeral = "IX";
                break;
            case 10:  romanNumeral = "X";
                break;
            default: romanNumeral = "";
                break;
        }
        System.out.print(romanNumeral);
    }
}```

```Java
import java.util.*;
import java.text.*;

public class SoftwareSales {

    public static void main(String[] args){
       	double discount, priceDiscount, price;
        System.out.print("Enter number of packages purchased:");
        Scanner keyboard = new Scanner(System.in);
        int quantity = keyboard.nextInt();
		price = 99* quantity;
		if (quantity >= 10 && quantity <=19){discount = price * .2; priceDiscount = price - discount;}
		else if (quantity >= 20 && quantity <=49){discount = price * .3; priceDiscount = price - discount;}
		else if (quantity >= 50 && quantity <=99){discount = price * .4; priceDiscount = price - discount;}
		else if (quantity >=100){discount = price * .5; priceDiscount = price - discount;}
		else { discount = 0; priceDiscount=price;}
		DecimalFormat dFormat = new DecimalFormat("0.00");
		System.out.println(" Your discount is: $"+ dFormat.format(discount));
		System.out.println("Your total is: $" + dFormat.format(priceDiscount));
    }
}```



```Java
import java.util.Scanner;

public class Runners {

    public static void main(String[] args) {
        // Basic i/o
		
        Scanner keyboard = new Scanner(System.in);
		System.out.print("Enter runner 1 name:");
        String runner1 = keyboard.nextLine();
		System.out.print(" Enter runner 1 time (in minutes):");
		int time1 = keyboard.nextInt();
		keyboard.nextLine();
		System.out.print(" Enter runner 2 name:");
		String runner2 = keyboard.nextLine();
		System.out.print(" Enter runner 2 time (in minutes):");
		int time2 = keyboard.nextInt();
		keyboard.nextLine();
		System.out.print(" Enter runner 3 name:");
		String runner3 = keyboard.nextLine();
		System.out.print(" Enter runner 3 time (in minutes):");
		int time3 = keyboard.nextInt();
        
		if (time1 < time2 && time1<time3){
			System.out.println(" "+runner1);
			if(time2<time3){
				System.out.println(runner2);
				System.out.println(runner3);
			} else{
				System.out.println(runner2);
				System.out.println(runner3);
			}
		} else if (time2 < time1 && time2<time3){
			System.out.println(" "+runner2);
			if(time1<time3){
				System.out.println(runner1);
				System.out.println(runner3);
			}else{
				System.out.println(runner3);
				System.out.println(runner1);
			}
		} else if (time3<time1 && time3<time2){
			System.out.println(" "+runner3);
			if(time1<time2){
				System.out.println(runner1);
				System.out.println(runner2);
			}else{
				System.out.println(runner2);
				System.out.println(runner1);
			}
		} else{
			System.out.println(" "+runner1);
			System.out.println(runner2);
			System.out.println(runner3);
		}
    }
}```

```Java
/**
 * @author Aaron Kolker
 * @version 1.0.0
 * TheSpeedOfSound
 */

import java.util.Scanner;
import javax.swing.JOptionPane;
//import java.io.*;
//import java.util.Random;

public class TheSpeedOfSound {

    public static void main(String[] args)  {
		//define variables
		String medium;
		String distanceInput;
		double distance;
		double travelTime;
		final String userMediumPrompt = "Enter one of the following: air, water, or steel: ";
		final String userDistancePrompt = "Enter the distance the sound wave will travel: ";
		final String userError = "Sorry, you must enter air, water, or steel.";
		final String air = "air";
		final String water = "water";
		final String steel = "steel";
		// User input
		System.out.print(userMediumPrompt);
		Scanner keyboard = new Scanner(System.in);
		medium = keyboard.nextLine();
		//////////////////////
		//calculate traveltime
		//////////////////////
		
		if (medium.equals(air)){
			//Prompt for distance
			System.out.print(userDistancePrompt);
			distanceInput = keyboard.nextLine();
			distance = Double.parseDouble(distanceInput);
			//calculate travelTime
			travelTime = distance/1100;
			//output travelTime
			System.out.print(" It will take " + travelTime + " seconds.");
			
		}
		else if (medium.equals(water)){
			//Prompt for distance
			System.out.print(userDistancePrompt);
			distanceInput = keyboard.nextLine();
			distance = Double.parseDouble(distanceInput);
			//calculate travelTime
			travelTime = distance/4900;
			//output travelTime
			System.out.println(" It will take " + travelTime + " seconds.");
		}
		else if (medium.equals(steel)){
			//Prompt for distance
			System.out.print(userDistancePrompt);
			distanceInput = keyboard.nextLine();
			distance = Double.parseDouble(distanceInput);
			//calculate travelTime
			travelTime = distance/16400;
			//output travelTime
			System.out.print(" It will take " + travelTime + " seconds.");
		}
		else {
			//Output error
			System.out.print(userError);
		}
		
		
    }
}```