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
