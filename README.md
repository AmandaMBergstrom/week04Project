"# week04Project" 
public class Week04CodingProject {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//1:
		//Create an array of int called ages
		int[] ages = {3, 9, 23, 64, 2, 8, 28, 93};
		
		//subtract the value of the first element from the value of the last element
		int result = ages[ages.length - 1] - ages[0];
		//print to console
		System.out.println("Age results " + result);
		
		//Create a new Array of int called ages2 with 9 elements
		int[] ages2 = new int[9];
		int ages2result = ages[ages.length - 1] - ages[0];
		//print to console
		System.out.println("Length of array:" + ages2result);
		
		//repeat the subtraction for ages2
		int result2 = ages2[ages2.length -1] - ages2[0];
		
		//Show using the index values for the elements is dynamic and use a loop
		//to iterate through the array and calculate the average age.
			int sum =0;
			for (int i =0; i < ages.length;i++) {
				sum +=ages[i];
			}
		
		
		
		//2:
		//Create an array of String called names
		String[] names = {"Sam", "Tommy", "Tim", "Sally", "Buck", "Bob"};
		double totalLetters = 0;
		for(String name : names) {
			totalLetters += name.length();
		}
		//Find the average number of letters per name
		double averageLetters = totalLetters / names.length;
		System.out.println("Average number of letters per name: " + averageLetters);
		//Add all the names together separated by spaces
		StringBuilder concatenateNames = new StringBuilder();
		for (String name : names) {
			concatenateNames.append(name).append(" ");
		} System.out.println("Concatenated names: " + concatenateNames.toString().trim()); }
		//3:How do you access the last element of any array?
	
	//Answer:
		// To access the last element in an Array you would use [thisArray.length - 1];
		// for example: int lastElement = thisArray[thisArray.length - 1];
		//This takes the length property of an Array and subtracts 1 to get the Index for the last element.

		//4:How do you access the first element of any array?
	
	//Answer
		//To access the first element in an array you would use thisArray[0];
		//for example: int firstElement = thisArray[0];
		//This retrieves the value stored in the first element/position of the Array with the index of 0.

		//5:
		//Previously created array called names:
		String[] names = {"Sam", "Tommy", "Tim", "Sally", "Buck", "Bob"};
	    //Create a new Array of int called nameLengths
		int[] nameLengths = new int[names.length];{
		//Write a loop to iterate over the names array and add the length of each name to nameLengths
		for(int i = 0; i < names.length; i++) {
			nameLengths[i] = names[i].length();
		}
		//6:
		//Write a loop to iterate over the nameLengths Array and calculate the sum of all the elements in the Array
		int sum = 0;
		for (int length : nameLengths) {
			sum += length;
		}
		
		//Print the result to the console
		System.out.println("Sum of the name Lengths: " + sum);
		}

		//7:
		//Write a method that takes a String, Word, and an Int, n, as arguments and returns the word concatenated to itself 
		//n number of times.
		public static String concatenatedWord(String word, int n) {
			StringBuilder result = new StringBuilder();
			for(int i = 0; i < n; i++) {
				result.append(word);
			}
			return result.toString();
		}
		
		
		//8:
		//Write a method that takes two Strings, firstName and lastName, and returns a full name
		public static String getFullName(String firstName, String lastName) {
	        return firstName + " " + lastName;
		}
	    
	     //9:
	     //Write a method that takes an Array of int and returns true if the 
		//sum of all the ints in the Array is greater than 100.
	    //Example for the output
		{
	     int[] numbers = {30, 40, 50, 60};
	     boolean result = isSumGreater(numbers);
	     System.out.println(result);
		}
	     //Method to check the sum of the integers
		public static boolean isSumGreater(int[]array) {
			int sum = 0;
			//to calculate the sum of the elements in the Array
			for(int num : array) {
				sum += num;
				//check the return
			} return sum > 100;
		}


		//10:
		// Write a method that takes an Array of double and returns the 
		//average of all the elements in the Array.		
		
		//Example:
			double[] numbers = {10.25, 21.75, 19.5, 33.25};
			double average = calculateAverage(numbers); 
			System.out.println("The average is: " + (average); 
			
			//Method to find average of elements
			public static double calculateAverage(double[] array) {
				if (array.length == 0) {
					//Can not divide by zero for an empty Array
					return 0.0; 
				}
			double sum = 0;
			
			//Find the sum of all elements
			for (double num : array) {
				sum += num;
				
				//Calculate the average
			} return sum / array.length;
}
			
			//11:
			//Write a method that takes two Arrays of double and returns true
			// if the average of the elements in the first Array is greater than
			//the average of the elements in the second Array
			//Example for question:
			public static void main1(String[] args) {
			double[] array1 = {15.5, 14.25, 16.75, 25.5};
			double[] array2 = {10.75, 17.5, 20.25, 9.25};
			
			boolean result = compareAverage(array1, array2);
			System.out.println(result); }
			//Method to check averages of elements
			public static boolean compareAverage(double[] array1, double[] array2) {
				double average1 = calculateAverage(array1);
				double average2 = calculateAverage(array2);
				
				return average1 > average2;
			}
			//Method to calculate the average of elements
			private static double calculateAverage1(double[] array) {
				if(array.length == 0) {
					return 0.0;
				}
				//Calculate the sum of all the elements
				int sum;
				for (double num : array) {
					sum += num;
				}
				//Calculate the average
				return sum/array.length; }

			
			//12:
			//Write a method called willBuyDrink that takes a boolean isHotOutside, and a double 
			//moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.
			//Example
		
			static boolean isHotOutside = true;
			double moneyInPocket = 18.25;
			
			boolean willBuyDrink = willBuyDrink(isHotOutside, moneyInPocket);
			System.out.println(willBuyDrink); 
			
			//Method to determine if we buy a drink
			public static boolean willBuyDrink(boolean isHotOuside, double moneyInPocket) {
			
			return isHotOutside && moneyInPocket > 10.50;
}		
			
			//13:
			//Create your own method 
			//Creating a method to calculate how many meals are necessary to feed a family of four for a week.
			public static void main11(String[] args) {
				int mealsPerDay = 3; //A person eats 3 meals per day
				int familySize = 4; //Family of four
				int daysInWeek = 7; //number of days in the week
				
				int totalMeals = calculateTotalMeals(mealsPerDay, familySize, daysInWeek);
				System.out.println("Total meals needed for the week: " + totalMeals);
			}
			//Method to calculate total meals
			public static int calculateTotalMeals(int mealsPerDay, int familySize, int daysInWeek) {
				return mealsPerDay * familySize * daysInWeek; }
}
			
