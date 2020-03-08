# Valid Palindrome
## https://leetcode.com/problems/valid-palindrome

Given a string, determine if it is a palindrome, considering only alphanumeric characters and ignoring cases.

Note: For the purpose of this problem, we define empty string as valid palindrome.
```
Example 1:

Input: "A man, a plan, a canal: Panama"
Output: true
Example 2:

Input: "race a car"
Output: false
```

# Implementation :

```java
class Solution {
    public boolean isPalindrome(String s) {
       if(s == null)
           return false;
       int left = 0;
       int right = s.length()-1;
       while(left < right){
           while(left < right && !Character.isLetterOrDigit(s.charAt(left)))
               left++;
           while(left < right && !Character.isLetterOrDigit(s.charAt(right)))
               right--;
           if(left < right && Character.toLowerCase(s.charAt(left++)) != Character.toLowerCase(s.charAt(right--))) 
              return false; 
       }
       return true; 
    }
}
```

# References :
https://www.youtube.com/watch?v=3RQ5ADUKHsY
