Document is a work under progress. There are some sample questions without their implementation. If you use this material in a class and you generate the code for it, make sure to make a pull request to update the doc.


#### Grocery store - just 5 products - ask the user for weights and compute the total price (with hard-coded per-pound prices)!
Write a program to perform check-out functionality for a simple Farmers Market store with exactly 5 products:

	Product	Price per pound
	Bananas	$ 0.44
	Apples	$ 0.99
	Cucumbers	$ 1.19
	Carrots	$ 0.89
	Oranges	$ 0.79

After getting the weight for each product purchase and compute & output the total purchase amount in the end. Do not use loops or arrays in this assignment. You can assume that all the user inputs are valid & the user will enter 0 for products (s)he does not purchase – no need to do any input validation explicitly. Use meaningful variable names & achieve "self-documenting" style of coding.
```java
import java.util.*;

public class GroceryStore {

    public static void main(String[] args) {
        // Rates
        double bananasRate = 0.44;
        double applesRate = 0.99;
        double cucumbersRate = 1.19;
        double carrotsRate = 0.89;
        double orangesRate = 0.79;

        // Weights
        double bananaWeight = 0;
        double appleWeight = 0;
        double cucumberWeight = 0;
        double carrotWeight = 0;
        double orangesWeight = 0;
        double grandTotal = 0;

        Scanner in = new Scanner(System.in);
        System.out.println("Enter the weights of all the items in the grocery store that you purchased!");
        System.out.println("If you didn't buy something, enter 0 for that item.");

        System.out.print("Enter weight of Bananas: ");
        bananaWeight = in.nextInt();
        System.out.println();

        System.out.print("Enter weight of Apples: ");
        appleWeight = in.nextInt();
        System.out.println();

        System.out.print("Enter weight of Cucumbers: ");
        cucumberWeight = in.nextInt();
        System.out.println();

        System.out.print("Enter weight of Carrots: ");
        carrotWeight = in.nextInt();
        System.out.println();

        System.out.print("Enter weight of Oranges: ");
        orangesWeight = in.nextInt();
        System.out.println();

        grandTotal = bananaWeight * bananasRate
                   + orangesWeight * orangesRate
                   + cucumberWeight * cucumberWeight
                   + appleWeight * applesRate
                   + carrotWeight * carrotsRate;

       System.out.println("The total amount due at checkout is: $" + grandTotal);
       System.out.println("Thank you for shpopping in the MicroTek grocery store!")
    }
}

```
#### Discounts
We will expand Program 1 using decision structure to apply discounts. Farmers market introduces two types of discounts to attract more customers and make each customer to purchase more.
	1.  Discount card program to attract customers. All customers who have signed up for it are considered as "special customers" and they get automatic minimum 10% discount off based on the total purchase amount. However, this cannot be combined with other discounts.
	2. All customers are eligible for the following discount program. If the total purchase is above $50, 5% discount will apply. If the total purchase exceeds $75, 10% discount will apply. If the total purchase exceeds $100, 15% discount will apply.

Do not allow the customer to combine the discounts. After computing the total purchase amount, program should determine the discount & output the following items if a discount is applied:
	- discount % and discount amount
	- discounted total

#### Another version
The loyalty card and amount based discount can be stacked!!

#### Weekly pay
Calculate weekly pay based on hourly rate and # of hours.
Overtime rate (50% more than regular rate) if the hours are > 40, but no pay beyond 50 hours.

#### Find the difference
Difference between 2 times specified in HH:MM:SS format.

#### Math practice
Practice +, -, * and / of random 2 numbers - keep track of how many correct out of 10 problems or so!

#### Guessing game
Think of a number between 1 and 100 in your mind. Then, your program should ask you minimal # of questions and determine your number based on your answers.
Program's question format will be
`Is it NN (<, =, >)?`
You can respond to that question in 3 ways: < indicates that your number is less than computer's guess, = means that program guessed your number right, and > means that your number  is greater than computer's guess.

` Guess a number between 1 and 100 (both inclusive)
and get ready to answer a few questions.
How about 50 (<,=,>)? <
How about 25 (<,=,>)? <
How about 12 (<,=,>)? >
How about 18 (<,=,>)? >
How about 21 (<,=,>)? <
How about 19 (<,=,>)? >
Your guess is 20
It was a good game!
Do you want to play again (y/n) ? y

Guess a number between 1 and 100 (both inclusive)
and get ready to answer a few questions.
How about 50 (<,=,>)? >
How about 75 (<,=,>)? <
How about 62 (<,=,>)? >
How about 68 (<,=,>)? >
How about 71 (<,=,>)? =
It was a good game!
Do you want to play again (y/n) ? y

Guess a number between 1 and 100 (both inclusive)
and get ready to answer a few questions.
How about 50 (<,=,>)? <
How about 25 (<,=,>)? <
How about 12 (<,=,>)? =
It was a good game!
Do you want to play again (y/n) ? n
`
Grocery store - tons of products from a file!

4101 BRAEBURN_REG      1 0.99
4021 DELICIOUS_GDN_REG 1 0.89
4020 DELICIOUS_GLDN_LG 1 1.09
4015 DELICIOUS_RED_REG 1 1.19
4016 DELICIOUS_RED_LG  1 1.29
4167 DELICIOUS_RED_SM  1 0.89
4124 EMPIRE 1 1.14
4129 FUJI_REG 1 1.05
4131 FUJI_X-LGE 1 1.25
4135 GALA_LGE 1 1.35
4133 GALA_REG 1 1.45
4139 GRANNY_SMITH_REG 1 1.39
4017 GRANNY_SMITH_LGE 1 1.49
3115 PEACHES 1 2.09
4011 BANANAS 1 0.49
4383 MINNEOLAS 1 0.79
3144 TANGERINES 1 1.19
4028 STRAWBERRIES_PINT 0 0.99
4252 STRAWBERRIES_HALF_CASE 0 3.99
4249 STRAWBERRIES_FULL_CASE 0 7.49
94011 ORGANIC_BANANAS 1 0.99

#### Lotto 6 distinct numbers
Explain srand() and rand() to generate random numbers in C++ programs. Write a method to generate & output 6 Lotto numbers - each number should be between 1 and 50 and the numbers should not be repeated. For example,

1 16 2 8 34 19 are valid Lotto numbers

8 16 2 8 34 19 is invalid, since 8 is repeated.

1 16 2 8 54 19 is invaid since we have 54 - outside the range.


#### Wordsearch game
Hardcode a word and display as

*********** (for the full length of that word)
Then, ask the neighbor to try to guess by typing one letter at a time.

#### Knapsack problems
Any 2 numbers, any 3 numbers, …
then any combination - Recursion!
