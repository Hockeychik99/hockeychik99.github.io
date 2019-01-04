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
