# Decimal-to-octal-conversion-using-Java

Decimal to octal conversion using java
In this article we will discuss decimal to octal conversion using java. For this purpose we need to ask a decimal number from user and convert that decimal number to its octal equivalent form and then print the converted number on to the screen.
decimal to octal conversion
Methods Discussed:-
Using an array to store the comparable octal value
Using int variable to store comparable octal value
Algorithm  ( Method 1 )
Take the decimal number from the user and store it in variable say decimal.
Create an array say octal to store the octal representation of the given decimal number.
Run a loop until decimal is not equal to 0 i.e., (decimal !=0)
Inside the loop insert the remainder that achieved by dividing decimal from 8 i.e., (decimal%8)
Coming out from the loop print the octal array in reverse order.
Decimal to octal conversion using Java
Related Pages
Hexadecimal to Decimal conversion

Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Binary to Octal conversion

Octal to Binary conversion

Java Code
Run
//Java program to convert decimal number to octal number
import java.util.Scanner;
public class Main
{
	public static void main(String args[])
	{   
		//scanner class object creation
		Scanner sc = new Scanner(System.in); 
		//Number
		int decimal = 148;
		//integer array for storing octal digits
		int octal[] = new int[20];
		int i = 0; 
		//writing logic for the conversion 
		while(decimal > 0)
		{       
			int r = decimal % 8;
			octal[i++] = r;
			decimal = decimal/8;
		}
		//printing result
		System.out.print("Octal number : ");
		for(int j = i-1 ; j >= 0 ; j--)
		System.out.print(octal[j]);
		//closing scanner class(not compulsory, but good practice)
		sc.close();
	}
}
Output
224
Algorithm  ( Method 2 )
Initialize ocatalNum to 0 and countVal to 1 and the decimal number as n
Find the remainder when decimal number divided by 8
Update octal number by octalNum + (remainder * countval)
Increase countval by countval*10
Divide decimal number by 8
Repeat from the second step until the decimal number is zero
Java Code
Run
// JAVA program to convert decimal
import java.io.*;
public class Main {

    // function to calculate the octal value of the given
    // decimal number
    static void octaltodecimal(int deciNum)
    {

        int octalNum = 0, countval = 1;
        int dNo = deciNum;

        while (deciNum != 0) {

            // decimals remainder is calculated
            int remainder = deciNum % 8;

            // storing the octalvalue
            octalNum += remainder * countval;

            // storing exponential value
            countval = countval * 10;
            deciNum /= 8;
        }
        System.out.println(octalNum);
    }

    // Driver Code
    public static void main(String[] args)
    {

        int n = 33;

        // Function Call
        octaltodecimal(n);
    }
}
Output
41
