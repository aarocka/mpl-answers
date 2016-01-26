# Chapter5

```Java
import java.util.Scanner;

public class Method_showChar {

    public static void main(String[] args){
        // Basic i/o
		System.out.print("Enter a line of text:");
        Scanner keyboard = new Scanner(System.in);
        String input = keyboard.nextLine();
       	System.out.print(" Enter your index:");
		String someOtherVar = keyboard.nextLine();
		int charPos = Integer.parseInt(someOtherVar);
		showChar(input, charPos);
    }
	
	public static void showChar(String x, int pos){
		char charAtPos = x.charAt(pos);
		System.out.print(" "+ charAtPos);
	}
}```

```Java
import java.util.Scanner;
public class TestAvgAndGrade {

    public static void main(String[] args){
        // Basic i/o
        System.out.print("Enter test grade for student 1:");
        Scanner keyboard = new Scanner(System.in);
        double a = keyboard.nextDouble();
		System.out.print(" Enter test grade for student 2:");
		double b = keyboard.nextInt();
		System.out.print(" Enter test grade for student 3:");
		double c = keyboard.nextInt();
		System.out.print(" Enter test grade for student 4:");
		double d = keyboard.nextInt();
		System.out.print(" Enter test grade for student 5:");
        double e = keyboard.nextInt();
		System.out.println(" The letter grades are as follows:");
		System.out.println("Student 1: " + determineGrade(a));
		System.out.println("Student 2: " + determineGrade(b));
		System.out.println("Student 3: " + determineGrade(c));
		System.out.println("Student 4: " + determineGrade(d));
		System.out.println("Studnet 5: " + determineGrade(e));
		System.out.println("The average grade was: " + calcAverage(a,b,c,d,e)+"0");
		
    }
	public static double calcAverage(double a, double b, double c, double d, double e){
		return (a + b + c + d + e)/5;
	}
	
	public static String determineGrade(double a){
		if (a >=90){return "A";}
		else if (a >=80 && a <=89){return "B";}
		else if (a>=70&&a <=79){return "C";}
		else if (a>=60&&a<=79){return "D";}
		else {return "F";}
	}
}
```