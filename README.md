# Reversing-a-Number-using-Recursion-in-Java

Reversing a Number using Recursion in java
Today we will discuss the program for reversing a number using recursion in Java programming language. We are given a number and need to print the reverse of the given number. We will discuss the both recursive and non-recursive method to find the reverse of the given input number.

Example :

Input : 1234
Output : 4321
Reversing a Number using Recursion in java
Method 1 (Using Recursion) :
Create a reverse(int n), a recursive function of void type.
Base condition will be : if (n <10)  , then print(n) and return.
Otherwise, print(n%10) and call function reverse(n/10).
Time and Space Complexity
Time Complexity : O(d) where, d denotes the number of digits in number n. Space Complexity : O(1)
Reversing a Number using Recursion in java
Code for Reversing a Number Using Recursion
Run
public class Main
{
public static void Reverse(int num)
    {
        // base condition to end recursive calls
        if (num < 10) {
            System.out.println(num);
            return;
        }
        else {
            // print the unit digit of the given number
            System.out.print(num % 10);
            // calling function for remaining number other than unit digit
            Reverse(num / 10);
        }
    }

    // driver code
    public static void main(String args[])
    {
        // number to be reversed
        int num = 1099;

        System.out.print("Reversed Number: ");
        // calling recursive function to print the number in reversed form
        Reverse(num);
    }
}
Output
Reversed Number: 9901
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Prime Number

Largest element in an array

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
Method 2
(1) Initialize rev_num = 0
(2) Loop over the number till the while num > 0
                   (a) Multiply the rev_num by 10 and add remainder of num divide by 10 to rev_num rev_num = rev_num*10 + num%10;

                   (b) Divide num by 10

(3) Return rev_num
Run
public class Main
{
static int reverseDigits(int num)
    {
        int rev_num = 0;
        while (num > 0) {
            rev_num = rev_num * 10 + num % 10;
            num = num / 10;
        }
        return rev_num;
    }
   // Driver code
   public static void main(String[] args)
  {
    int num = 4562;
    System.out.println("Reverse of no. is " + reverseDigits(num));
   }
 }
Output
Reverse of no. is 2654
