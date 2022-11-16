- 👋 Hi, I’m @MeghanaN04

Typing Speed Calculator-Code

package firstjavaproject;

import java.time.LocalTime;

import java.util.Random;

import java.util.Scanner;

import java.util.concurrent.TimeUnit;

public class WPM {
  static String[] words = {"envelope","cantelope","the","hello","microscope","elephant","biscuit","hammer","went","cap"};
	
public static void main(String[] args ) throws InterruptedException {
	System.out.println("3");
	TimeUnit.SECONDS.sleep(1);
	
	System.out.println("2");
	TimeUnit.SECONDS.sleep(1);
	
	System.out.println("1");
	TimeUnit.SECONDS.sleep(1);
	
	Random rand = new Random();
	for(int i = 0; i<10; i++) {	
	System.out.print(words[rand.nextInt(9)] + " ");
	
}
	System.out.println();
	double start = LocalTime.now().toNanoOfDay();
	
	Scanner scan = new Scanner(System.in);
	String typedwords = scan.nextLine();
	double end = LocalTime.now().toNanoOfDay();
	double elapsedTime = end - start;
	double seconds = elapsedTime / 1000000000.0;
	int numChars = typedwords.length();
	// (x characters / 5 ) / 1min = y WRM
	int wpm = (int) ((((double) numChars / 5) / seconds) * 60 );
	
	System.out.println("Your wpm is " + wpm + "!");
	


Output:
3
2
1
biscuit hello envelope microscope hello the microscope hello elephant microscope 
paris is a beautiful place
Your wpm is 29!

