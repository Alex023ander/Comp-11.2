# Comp-11.2


import java.util.Scanner;
public class Comp112 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
		String newString = "";
		System.out.println("enter string or DONE when finished");
		String userInput = "";
		while(!userInput.equalsIgnoreCase("DONE")){
			newString+=userInput+"\t";
			userInput = input.nextLine();
			if(userInput.length()>=20){
				try {
					throw new StringTooLongException();
				}
				catch (StringTooLongException ex) {
					System.out.print(ex.getMessage()+"\nEnter a string. Be aware that the limit is 20 characters long.\n");
					userInput="";
				}
			}
		}
		System.out.println("The letters are :");
		System.out.println(newString);
	}
}
