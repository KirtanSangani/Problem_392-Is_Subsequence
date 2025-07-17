# Problem_392-Is_Subsequence

7/17/2025

## Thought Process
My initial thought process behind the problem was to actually traverse through the String s and whenever a letter appears that is not in the String t, I return False. This would work with most test cases, as the String t would have the characters in order; however, some of the latter test cases were not in order and it would return True when it was supposed to return false. 

##  Initial Solution
I initially created a for loop traversing String s, and would see if the character at index i was in String t, if it was, I would delete that letter from t. I would do this by setting t to equal t[:t.index(s[i],0)] + t[t.index(s[i],)+1:]. I realized later that this was not optimal and would later change it. This solution worked for some cases but not all cases.

Initial solution - N/A 

Complexity - O(len(s))

## Final Solution
I decided that instead of traversing through String s, I would traverse thorugh String t. I also understood that I needed to look so the characters in String s in order, so decided to traverse through String t looking at the first index of String s until there was a match. When there is a match, I would add 1 to the a count variable I created before the for loop. The way it would return True is if count is equal to the length of s, meaning that every character was found. To solve all edge cases, I created an if statement at the beginning seeing if the length of s is equal to 0. If so, I would return True. Additionally, if count is equal to the length of s before the for loop ends, I would return True from within the for loop. 

Final Solution - 3 ms

Complexity - O(len(t))

## Takeaways
I learned that edge cases are important and to have code in which every single case is taken apart of, especially if it is just one if statement for one specific edge case, is necessary for good, efficient code. 