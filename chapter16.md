# Chapter16

```Java
import java.util.*;

public class Member {
		
    public static void main(String[] args) {
        // Basic i/o
		Scanner keyboard = new Scanner(System.in);
        System.out.print("Enter size of array:");
		String input = keyboard.nextLine();
		int sizeOfArray = Integer.parseInt(input);
		
		int[] myIntArray = new int[sizeOfArray];
		
		for(int i = 0; i < sizeOfArray; i++){
			System.out.print("Enter number for array index " + i + ":");
			input = keyboard.nextLine();
			myIntArray[i] = Integer.parseInt(input);
		}
		
		
        System.out.print("Enter number to search for in array:");
		input = keyboard.nextLine();
		int search = Integer.parseInt(input);
		
		if(isMember(myIntArray, search)){System.out.println("true");}
		else{System.out.println("false");};
		
    }
	
	public static boolean isMember(int[] array, int value) {
		if(array.length == 0) {return false;}
		if(array[0] == value) {return true;}
    	int[] array2 = new int[array.length-1];
    	System.arraycopy(array,1,array2,0,array2.length);
    	return isMember(array2, value);          
	}
}
```

```Java
import java.util.Scanner;

public class StringReverse {

    public static void main(String[] args) {
        // Basic i/o
        System.out.print("Enter a string to be reversed:");
        Scanner keyboard = new Scanner(System.in);
        String name1 = keyboard.nextLine();
        System.out.print(reverse(name1));
    }
	public static String reverse(String s){
    if (s.length() == 0) 
         return s;

    return reverse(s.substring(1)) + s.charAt(0);
}
}
```

```Java
import java.util.Scanner;
public class Multiplication {

    public static void main(String[] args) {
        // Basic i/o
        System.out.print("Enter a value for x:");
        Scanner keyboard = new Scanner(System.in);
        int x = keyboard.nextInt();
		System.out.print("Enter a value for y:");
		int y = keyboard.nextInt();
		System.out.print("The product of " + x + " * " + y + " is " + product(x,y));
    }
	
	public static int product(int num1, int num2) { 
    if (num1 == 0 || num2 == 0) {
        return 0;
}

else if( num2 < 0 ) {
    return - num1 + product(num1, num2 + 1);
}

else {
    return num1 + product(num1, num2 - 1);
}
	}
}
```

```Java
import java.util.Scanner;
public class Palindrome {
    public static void main(String[] args){
        // Basic i/o
        System.out.print("Enter a phrase:");
        Scanner keyboard = new Scanner(System.in);
        String test = keyboard.nextLine();
		test = test.replaceAll("\\W", "");
		test = test.toLowerCase();
		if(isPalindrome(test)){
			System.out.print("That phrase is a palindrome.");
		}else{
			System.out.print("That phrase is not a palindrome.");
		}
		
    }
	
	public static boolean isPalindrome(String word) {
		
			
  			if(word.length() < 2) { return true;  }
  			char first  = word.charAt(0);
  			char last   = word.charAt(word.length()-1);
  			if(  first != last  ) { return false; }
  			else { return isPalindrome(word.substring(1,word.length()-1)); }
		
}
}
```

```Java
import java.util.Scanner;

class SumofNumbers {

    public static void main(String[] args)  {
        // Basic i/o
        System.out.print("Enter a number:");
        Scanner keyboard = new Scanner(System.in);
        int input = keyboard.nextInt();
		while(input < 0){
			System.out.print("Enter a positive value:");
			input = keyboard.nextInt();
		}
		System.out.print("The sum of all numbers up to " + input + " is " + sum(input));
    }
	public static int sum(int n) {
            if (n == 0)
            {
                        return 0;
            }
			else if (n == 1) {
				return 1;
			}
            else
            {
                        return (sum(n-1) + n);
            }
}
}
```

```Java
Lol i couldn't figure this one out. YOLO!
```