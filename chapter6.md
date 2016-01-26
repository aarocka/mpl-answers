# Chapter6

```Java
import java.util.Scanner;
import java.text.*;
public class Car{
	        
    // Fields
	private int yearModel;
    private String make;
    private int speed;
        
    // the Bicycle class has
    // one constructor
    public Car(int y, String m){
        yearModel = y;
        make = m;
        speed = 0;
    }
	    public void setYearModel(int year){
        yearModel = year;
    }


    /**
     * This method sets the value of make.
     * @param m The make of the car.
     */
    public void setMake(String m){
        make = m;
    }

    /**
     * This method sets the value of speed
     * @param currentSpeed The current speed of the car.
     */
    public void setSpeed(int currentSpeed){
        speed = currentSpeed;
    }

    /**
     Accessor method getYearModel returns the year model of the car.
     @return The car's year model.
     */
    public int getYearModel(){
        return yearModel;
    }

    /**
     Accessor method getMake returns the make of the car.
     @return The car's year model.
     */
    public String getMake(){
        return make;
    }

    /**
     Accessor method getSpeed returns the current speed of the car.
     @return The car's current speed.
     */
    public int getSpeed(){
        return speed;
    }
    /**
     Method accelerate increases the speed by five.
     */
    public void accelerate() {
        speed = speed + 5;
    }

    /**
     Method brake decrease the speed by five.
     */
    public void brake() {
        speed = speed - 5;
    }	
	
	public static void main(String[] args){
		
		Car car = new Car(2004, "something");
		
		for(int i=1; i<=5; i++){
			car.accelerate();
			System.out.println(car.getSpeed());
		}
		for(int i=1; i<=5; i++){
			car.brake();
			System.out.println(car.getSpeed());
		}
		
		
		
	}
}
```

```Java
import java.util.Scanner;
import java.text.*;
public class Payroll{
	        
    // Fields
    private String name;
	private int idNumber;
	private double rate;
	private int hours;
        
    // the Bicycle class has
    // one constructor
    public Payroll(String n, int i) {
        name = n;
		idNumber = i;
    }
	
	public String getName(){return name;}
    public int getidNumber(){return idNumber;}
    public double getRate(){return rate;}
    public int getHours(){return hours;}
	public void setName(String x){name = x;}
	public void setidNumber(int x){idNumber =x;}
	public void setRate(double x){rate = x;}
	public void setHours(int x){hours = x;}
	public double grossPay(){return hours * rate;}
	public static void main(String[] args){
		Scanner keyboard = new Scanner(System.in);
		
		System.out.print("Enter employee's name:");
        String name = keyboard.nextLine();
		
		System.out.print("Enter employee's ID number:");
		String input = keyboard.nextLine();
		int id = Integer.parseInt(input);
		
		System.out.print("Enter hourly rate:");
		input = keyboard.nextLine();
		double rate = Double.parseDouble(input);
		
		System.out.print("Enter number of hours worked:");
		input = keyboard.nextLine();
		input = input.replace(",", "");
		int hours = Integer.parseInt(input);
		
		Payroll payroll = new Payroll(name, id);
		payroll.setRate(rate);
		payroll.setHours(hours);
		DecimalFormat dFormat = new DecimalFormat("0.00");
		System.out.print(payroll.getName() + ", employee number " + payroll.getidNumber() + ", made $" + dFormat.format(payroll.grossPay())+ " in gross pay.");
		
		
	}
}
```

```Java
import java.util.Scanner;
class Temperature{
	private double ftemp;
	public Temperature(double t){ftemp=t;}
	public void setFahrenheit(double t){ftemp = t;}
	public double getFahrenheit(){return ftemp;}
	
	public double getCelsius(){
		//System.out.println(ftemp);
		//System.out.println((5/9));
		return ((5.0/9.0) * (ftemp-32.0));
		}
	public double getKelvin(){
		return  ((5.0/9.0) * (ftemp - 32.0)) + 273.0 ;
		}
	public static void main(String[] args){
		Scanner keyboard = new Scanner(System.in);
		System.out.print("Enter a Fahrenheit temperature:");
		String input = keyboard.nextLine();
		double f = Double.parseDouble(input);
		Temperature temp = new Temperature(f);
		System.out.println("The temperature in Fahrenheit is "+ temp.getFahrenheit());
		System.out.println("The temperature in Celsius is "+ temp.getCelsius());
		System.out.println("The temperature in Kelvin is "+ temp.getKelvin());
	}
}
```