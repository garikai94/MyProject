# MyProject
package lisacancode;
// The program will check the test time and input the seconds taken
//The program will also randomly generate a number
import java.util.Scanner;

public class WhatDoesThisAppDo {

	public static void main(String[] args) {
		final int number = 5;
        int value = 0; int value2 = 0;
        // The method must check and return current time in millisecond
        long startTime = System.currentTimeMillis();
        String string1= " ";
        Scanner string2 = new Scanner(System.in);


        while (value < number){
            int number1 = (int) (Math.random() * 10);
            int number2 = (int) (Math.random() * 10);
            
            if (number1 < number2){
                int temp = number1;
                number1 = number2;
                number2 = temp;
                value++;  // Increase the correct answer
            }
            System.out.println("What is "+ number1 + " = " + number2 + "?");
            int answer = string2.nextInt();
            
            if (number1 - number2 == answer){   System.out.println(" You " + "are correct!");
            value2++; // Increase the correct answer
            }
            else
                System.out.println("Your answer is wrong.\n" + number1 +
                        ((number1 - number2 == answer) ? "correct": "wrong"));
        }
        // Returning the time taken
        long endTime = System.currentTimeMillis();
        long testTime = endTime - startTime;
        System.out.println("Correct count is" + value2 + "\nTest time is " + testTime/100
                + "seconds\n" + string1);
	}

}
