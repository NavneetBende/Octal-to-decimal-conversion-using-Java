# Octal-to-decimal-conversion-using-Java

Octal to decimal conversion using java
 
In this article we will discuss octal to decimal conversion using java. For this purpose we need to ask an octal number from user and convert that octal number to its decimal equivalent form and then print the converted number on to the screen.
Octal to decimal conversion using java
Algorithm
Declare two variables, one for storing decimal value and second for storing value of the power.
Use  the while loop till octal number entered by user is greater than 0.
Use a statement to get the last digit of the octal number.
Use the statement for adding each digit by multiplying by the power of 8 and power starts with 0 till p-1 (where p is the number of digits in the octal number) by using power function.
Use the statement for removing last digit of the octal number and taking only remaining number and increase the value of the power by 1.
Repeat the steps 3 to 6 till the value of the loop does not gets false.

Java Code :
Run
//Java program to convert octal number to decimal number
import java.util.Scanner;
public class Main
{
	public static void main(String args[])
	{      
		//scanner class object creation
		Scanner sc = new Scanner(System.in);    
		//input from user
		System.out.print("Enter a octal number : ");
		int octal = sc.nextInt();
		//Declare variable to store decimal number  
		int decimal = 0;
		//Declare variable to use in power		
		int n = 0;  
		//writing logic for the conversion
		while(octal > 0)
		{
			int temp = octal % 10;  
			decimal += temp * Math.pow(8, n);  
			octal = octal/10;  
			n++;  
		}
		//printing result
		System.out.println("Decimal number : "+decimal); 
		//closing scanner class(not compulsory, but good practice)
		sc.close();   
	}
}
Output :
Binary Number is 512
Decimal Number is 330
