## Day 5 (and it's not January 5th, life gets in the way sometimes)
So, yeah... sometimes my weekends are boring with nothing to do, other times I barely get a chance to sit down. That was this past weekend. My son had a merit badge thing for scouts, I had a hockey game Saturday and Sunday, my wife had a hockey game Sunday, son had lacrosse tryouts Saturday night, daughter went ice skating ... didn't even think about turning on the laptop. Monday and Tuesday were whirlwind days as well. Tuesday I turned on the laptop, but that was to do homework and some other important things I had to get to. So here it is, Wednesday, and I'm on day 5. Now to code.

I get emails from Code Wars with suggested katas. There was one in the email I wanted to try, but when I logged in today, it wasn't the first one that I saw, and it didn't come up before choosing this one:

## Description
```
After a hard quarter in the office you decide to get some rest on a vacation. So you will book a flight for you and your girlfriend and try to leave all the mess behind you.

You will need a rental car in order for you to get around in your vacation. The manager of the car rental makes you some good offers.

Every day you rent the car costs $40. If you rent the car for 7 or more days, you get $50 off your total. Alternatively, if you rent the car for 3 or more days, you get $20 off your total.

Write a code that gives out the total amount for different days(d).
```

## My Code
```
public class Kata {
  public static int rentalCarCost(int d) {
    // Your solution here
    int total = 0;
    final int DAILY_RENTAL = 40;
    final int SEVEN_DAY_DISCOUNT = 50;
    final int THREE_DAY_DISCOUNT = 20;
    
    if (d >= 7) {
       total = (d * DAILY_RENTAL) - SEVEN_DAY_DISCOUNT;
    }
    else if (d < 3) {
       total = d * DAILY_RENTAL;
    }
    else {
       total = (d * DAILY_RENTAL) - THREE_DAY_DISCOUNT;
    }
    return total;
  }
}
```
I liked this kata. It was very realistic and made sense to why I would write a code for this type of scenario. Again, I realize my code is a little wordy. After I got to the `else` statement, I realized I could have figured `total = d * DAILY_RENTAL` above the `if` loop and the amount in `total` would carry into the loop and I could just subtract the appropriate discount. Starting to come a little easier in certain aspects (even after a several day break!)

---------------------------------------------------------------------------------------------------------------

## Day 4 (I think... yes, today is January 4, 2019...)

So I had some time early in the day and decided to use my time wisely and see if I could knock out some code before going on a dog walk. I perused Code Wars and found a few katas that I should know how to do, but I knew I'd learn better with a little help from a peer, so I kept looking. And whaddaya know, I found one I could handle!

So, since I've been taking the long way around in the previous days, I knew I could use a `for` loop and use the simplified method.

## Description
```
Summation
Write a program that finds the summation of every number from 1 to num. The number will always be a positive integer greater than 0.

For example:

summation(2) -> 3
1 + 2

summation(8) -> 36
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8
```

## My code
```
public class GrassHopper {

    public static int summation(int n) {
       int i = 0;
       int total = 0;
       
       for (i = n; i > 0; i--) {
          total += i;
       }

        return total;
    }
}
```

Had a few slight issues at first, but very minor tweaks and it worked! Looking through the other solutions, there are still ways I could have condensed it further, but overall I'm happy with my solution. I also wrote the code to start with the number given and add one less to it with each iteration. But since addition is commutative, this works! :) So, it's not even noon yet and Day 4 of 100 Day of Code is finished!!! (Might have some bonus "episodes" later!)

_______________________________________________________________________________________________________________

## Day 3

So here it is.. another day and I'm still at it. Sometimes I think I get myself in over my head. School is still on winter break and resumes on Monday. So I've been trying to get a head start, but was waiting on an email from Cisco. Finally got that today, got my account active and excited to get a jump start on learning Linux. 

So.... I really don't know how long this took me (but it was a lot longer than I thought it would). I almost thought I was going to give it up because I thought I was really missing something (stupid integer division). Here's the prompt from Code Wars:

```
Your task is to write a function which returns the sum of following series upto nth term(parameter).

Series: 1 + 1/4 + 1/7 + 1/10 + 1/13 + 1/16 +...
Rules:
You need to round the answer to 2 decimal places and return it as String.
If the given value is 0 then it should return 0.00
You will only be given Natural Numbers as arguments.

Examples:
SeriesSum(1) => 1 = "1.00"
SeriesSum(2) => 1 + 1/4 = "1.25"
SeriesSum(5) => 1 + 1/4 + 1/7 + 1/10 + 1/13 = "1.57"
```

And wallah my working code:

```
public class NthSeries {
	
	public static String seriesSum(int n) {
		// Happy Coding ^_^		
    String finalNum = "";
    double total = 0.0;
    int counter = 0;
    int denominator = 1;
    double fraction = 0.0;
    
    if (n == 0) {
       finalNum = "0.00";
       return finalNum;
    }
    else {
       while (counter != n) {
          counter++;
          fraction = 1.0 / denominator;
          total += fraction;
          denominator += 3;
       }
    return String.format("%.2f", total);
    }
	}
}
```

Annnnnnnnnnnd of course since I can now see the other solutions, I could have done this all in about 3 lines.... ho hum... I'll get there. Trying to figure out how to format to two decimal places actually took up a lot of the time I spent on this. I tried looking through the Java documentation but had trouble finding what I needed. So thankfully, to my rescue, a fellow SNHU student was able to help me figure that out (Thanks J.D.!) Now, onto Linux!

__________________________________________________________________________________________________________________

## Day 2 of 100 Days of Code

I was tired tonight, and have a headache, but I opened Code Wars and found a kata challenge I thought I could handle. And to my surprise (and after finding the missing brace) I did it. I know the point of coding, and especially learning how to code, is not to get it right on the first try. But being that I'm still very much a newbie, when the code I write works the first time, it is a huge pat on my back and reinforces that I actually have learned something. My goal for this 100 days of code challenge is to get more comfortable writing code. And have the confidence to know that I do know what I'm doing so when the code doesn't compile, I have enough understanding to review it to see where I went wrong and how to fix it.

I love math. So when I find challenges like the one I did today, I feel that I should be able to understand what is going on behind the code (well, other than the fact that I'm the one writing the code). But I am a visual person when it comes to math, and if I am not using concrete figures I sometimes (okay, most of the times) get lost. So while figuring out this challenge, and what exactly needed to be done, I had to use an example with exact numbers. This showed me that my original thinking of just adding one to a `total` variable was not what I wanted.


## Description:
```
Given two integers a and b, which can be positive or negative, find the sum of all the numbers between 
including them too and return it. If the two numbers are equal return a or b.

Note: a and b are not ordered!
```
## My Solution:
```
  public class Sum
  {
     public int GetSum(int a, int b)
     {
      //Good luck!
      int firstNum = a;
      int secondNum = b;
      int total = 0;
      int nextNum = 0;
      
      if (firstNum == secondNum) {
         return firstNum;
      }
      else {
         if (firstNum < secondNum) {
            nextNum = firstNum;
            while (nextNum <= secondNum) {
               total += nextNum;
               nextNum++;
            }
         }
         else {
            nextNum = secondNum;
            while (nextNum <= firstNum) {
               total += nextNum;
               nextNum++;
            }
         }
      return total;
      }
     }
  }
```
So my code is wordy. After seeing some of the other solutions, there is room for improvement to condense some of the code. I'm sure that will come with time. I'm just pretty stoked I was able to do it!
