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
