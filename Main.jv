// Daniel Davis
// Change Calculator - Calculates how much change is due given two amounts of money.
// Also describes what currency units are needed(USD)
// start date: 7/26/16

import javax.swing.JOptionPane;

public class ChangeCalc {
	
	//Functions//
	public static double difference(double total, double payment) { // calculates the difference between the amount due and the amount payed
		double result = payment - total;
		return result;
	} // end of difference function
	
	public static double roundToDecimals(double d, int c) { // rounds the doubles to the nearest one-hundredths place
	   int temp = (int)(d * Math.pow(10 , c));  
	   return ((double)temp)/Math.pow(10 , c);  
	} // end of round to decimals function
	
	
	public static String calc(double amount) { // calculates the amount of USD currency units to dispense as change
		double tmp;
		String result = "Change Due: ";
		
        if(amount >= 100) {
            tmp = amount/100;
            result = result + (int)tmp + " $100 bill(s) ";
            amount = amount % 100;
        } // end of if
        if(amount >= 50) {
            tmp = amount/50;
            result = result + (int)tmp + " $50 bill(s) ";
            amount = amount % 50;
        } // end of if
        if(amount >= 20) {
            tmp = amount/20;
            result = result + (int)tmp + " $20 bill(s) ";
            amount = amount % 20;
        } // end of if
        if(amount >= 10) {
            tmp= amount/10;
            result = result + (int)tmp + " $10 bill(s) ";
            amount = amount % 10;
        } // end of if
        if(amount >= 5) {
            tmp = amount/5;
            result = result + (int)tmp + " $5 bill(s) ";
            amount = amount % 5;
        } // end of if
        if(amount >= 1) {
            tmp = amount/1;
            result = result + (int)tmp + " $1 bill(s) ";
            amount = amount % 1;
        } // end of if
        if(amount >= .25) {
            tmp = amount/.25;
            result = result + (int)tmp + " qurter(s) ";
            amount = amount % .25;
        } // end of if
        if(amount >= .10) {
            tmp = amount/.10;
            result = result + (int)tmp + " dime(s) ";
            amount = amount % .10;
        } // end of if
        if(amount >= .05) {
            tmp = amount/.05;
            result = result + (int)tmp + " nickel(s) ";
            amount = amount % .05;
        } // end of if
        if(amount >= .01) {
            tmp = amount / .01;
            result = result + (int)tmp + " penny(s) ";
            amount = amount % .01;
        } // end of if
        if(amount < 0) {
        	JOptionPane.showMessageDialog(null, "Please Insert More Change.");
        } // end of if
        return result;

	} // end of calc function
	
	//Main//
	public static void main(String[]args) {
			
		//first screen//
		// receiving the amount due and the payment amount and storing them in local variables
		String Total = JOptionPane.showInputDialog("Welcome to Change Calculator." + "\nPlease enter the total amount due:");
		double total = 0.0;
		
		for(int i=0; i<Total.length(); i++) { // goes through the text to make sure it's just doubles
			if(Total.matches("[0-9.]*")) {
			total = Double.parseDouble(Total);
			} // end of if
			else {
				JOptionPane.showMessageDialog(null, "Invalid input. Please use only numbers and a decmial.");
				main(null);
			} // end of else 
		} // end of for loop
		
		//second screen//
		String Payment = JOptionPane.showInputDialog("Please enter the amount being payed: ");
		double payment = 0.0;
		
		for(int i=0; i<Payment.length(); i++) { // goes through the text to make sure it's just doubles
			if(Payment.matches("[0-9.]*")) {
			payment = Double.parseDouble(Payment);
			} // end of if
			else {
				JOptionPane.showMessageDialog(null, "Invalid input. Please use only numbers and a decmial. ");
				main(null);
			} // end of else 
		} // end of for loop
		
		// see the difference
		double diff = difference(total, payment);
		diff = roundToDecimals(diff, 2);

		
		//DEBUGGING
		System.out.println(total);
		System.out.println(payment);
		System.out.println(diff);
		//DEBUGGING
		
		// final result/screen
		String Result = calc(diff);
		String Diff = Double.toString(diff);
		JOptionPane.showMessageDialog(null, "The amount of change due is: " + Diff);
		JOptionPane.showMessageDialog(null, Result);
		
	} // end of main
	
} // end of class
