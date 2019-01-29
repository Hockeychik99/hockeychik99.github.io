## Day 10 (January 29, 2019)
I'm back. And picked, what I thought, was an easy kata from Code Wars since I need to leave shortly. There was some chatter about practicing coding by some other students, so it was suggested I pick one and post it. So I did. I needed Google's help for this one even though it is fairly easy. Apparently, this specific method was not covered in my class, or I did not take good enough notes when we covered this. Either way, my initial attempts failed, so once Google showed me the way, I got the green lights!

## Description
```
We need a function that can transform a string into a number. 
What ways of achieving this do you know?

Note: Don't worry, all inputs will be strings, and every string 
is a perfectly valid representation of an integral number.
```

## My Code
```
public class StringToNumber {
  public static int stringToNumber(String str) {
    //TODO: Convert str into a number
    int strInt = 0;
    strInt = Integer.parseInt(str);
    return strInt;
  }
}
```

____________________________________________________________________________________________________________________________________

## Day 9.5 (coding twice in one day!?)
Instead of working, I decided to jump back on ZyBooks and start the last chapter that wasn't covered in my class last term (thanks to another friend who asked me if I knew of any other Java resources to learn from). So I worked through the first lesson `Do-while Loops`. I'm not going to post the code, but I was able to work through the two activities provided in the section and passed when it was checked. The low-down of `do-while loops` is that a condition will execute at least one time. 
```
do {
  something
} while (until some condition is met);
```
So that's your double-dose of code for today!

___________________________________________________________________________________________________________________________________

## Day 9 (feeling like a failure with this 100 days of code thing...)
So, it is January 25, 2019 and I am only on day 9 of 100 days of code. I did open Code Wars yesterday and read through a few katas but my brain was mush and just said to close it before getting frustrated. But I am here today, and I did code something. Semi proud of myself as well (I'll explain after posting the code)

## Description
```
Given two numbers and an arithmetic operator (the name of it, as a string), 
return the result of the two numbers having that operator used on them.

a and b will both be positive integers, and a will always be the first number 
in the operation, and b always the second.

The four operators are "add", "subtract", "divide", "multiply".
```

## My Code
```
class ArithmeticFunction {
  public static int arithmetic(int a, int b, String operator) {
    // your code here
    int total = 0;
    
    if (operator.equals("add")) {
       total = a + b;
    }
    
    else if (operator.equals("subtract")) {
       total = a - b;
    }
    
    else if (operator.equals("multiply")) {
       total = a * b;
    }
    
    else {
       total = a / b;
    }
    
    return total;
  }
```
So, the instructions also stated to try it without using `if` statements. Well, I'll take that fail. I don't think I understand enough of this to do it without `if` statements. Maybe with a `replace` function? I'll pester my code-knowing friends and see if they can help me figure out another way to do it. So my pat-myself-on-my-back moment: while I was in IT-145 (java) at SNHU, I was trying to do a similar thing of comparing string input but I was using `if (operator == 'add')` and wasn't getting the results I was expecting. I was like what am I doing wrong? What am I missing!? A very helpful and knowledgeable friend mentioned to use the `.equals` instead for string comparisons because the `==` actually uses the ASCII values to compare so if they don't match up, the program will throw wonky results. So, from that point, I said I would always remember that because it had been so frustrating to me. So I tried the `.equals` first in the code above (and it worked!!!)

If I come up with another solution, I will add it here and reference Day 9. Maybe, someday, it'll happen!
(Just submitted the kata and I see to not use `if` statements I should have used the `switch` function! I actually did know that (just forgot about it). 

__________________________________________________________________________________________________________________________________

## Day 8
So I tried. I really tried. I've been sitting at my laptop most of the evening, revamping my resume and writing a cover letter for a job I'm applying for and since I don't know how to do anything without multitasking I pulled up Code Wars and found a kata I wanted to try. But when I clicked on it (and eventually went back to see what it said) it had failed to load. And it is now really past my bedtime. So I tried. I did. Tomorrow is another day to try again.

_________________________________________________________________________________________________________________________

## Day 7
Yay! Back to consecutive days of coding! There was a kata on Code Wars that was mathematical in nature and I wanted to do it, but it dealt with arrays and I have very limited knowledge and really didn't feel like getting stuck and frustrated tonight. So the next one was fairly easy - at least I understood the logic and was hoping the way I was thinking it through would work. Alas, it did! =o)

## Description
```
Timmy & Sarah think they are in love, but around where they live, 
they will only know once they pick a flower each. If one of the 
flowers has an even number of petals and the other has an odd 
number of petals it means they are in love.

Write a function that will take the number of petals of each 
flower and return true if they are in love and false if they aren't.
```

## My Code
```
public class OppositesAttract {

  public static boolean isLove(final int flower1, final int flower2) {
  if (flower1 != flower2) {
     if ((flower1 % 2 == 0 && flower2 % 2 != 0) || (flower1 % 2 != 0 && flower2 % 2 == 0)) {
        return true;
     }
     else {
        return false;
     }
  }
  else {
     return false;
  }

  }
  
}
```
Looking over some of the other submitted solutions, there were some one and two line solutions. Totally didn't think about the `isEven` or `isOdd` functions (is that what they are called?! I'm drawing a blank, but it's late). But overall, I'm happy with my solution. It's not too bulky and I was able to include the correct logic, using `&&` and `||` for the correct expressions.

___________________________________________________________________________________________________________________

## Day 6 .... only about a week behind ...
Again, life. But I'm here. Now. Today (January 15, 2019). Decided to take on an easy kata on CodeWars (and I still had to Google because I realized the method I learned to do this was using a Stream and I knew there had to be a simpler way).

## Description
```
We need a function that can transform a number into a string.

What ways of achieving this do you know?
```

## My Code
```
class Kata {
  public static String numberToString(int num) {
    // Return a string of the number here!
    String convertNum = "";
    
    convertNum = Integer.toString(num);
    return convertNum;
  }
}
```
So, there ya have it. Day 6 completed. 

--------------------------------------------------------------------------------------------------------

## Day 5 (and it's not January 5th, life gets in the way sometimes)
So, yeah... sometimes my weekends are boring with nothing to do, other times I barely get a chance to sit down. That was this past weekend. My son had a merit badge thing for scouts, I had a hockey game Saturday and Sunday, my wife had a hockey game Sunday, son had lacrosse tryouts Saturday night, daughter went ice skating ... didn't even think about turning on the laptop. Monday and Tuesday were whirlwind days as well. Tuesday I turned on the laptop, but that was to do homework and some other important things I had to get to. So here it is, Wednesday, and I'm on day 5. Now to code.

I get emails from Code Wars with suggested katas. There was one in the email I wanted to try, but when I logged in today, it wasn't the first one that I saw, and it didn't come up before choosing this one:

## Description
```
After a hard quarter in the office you decide to get some 
rest on a vacation. So you will book a flight for you and 
your girlfriend and try to leave all the mess behind you.

You will need a rental car in order for you to get around 
in your vacation. The manager of the car rental makes you 
some good offers.

Every day you rent the car costs $40. If you rent the car 
for 7 or more days, you get $50 off your total. Alternatively, 
if you rent the car for 3 or more days, you get $20 off your total.

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
Write a program that finds the summation of every 
number from 1 to num. The number will always be a 
positive integer greater than 0.

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
