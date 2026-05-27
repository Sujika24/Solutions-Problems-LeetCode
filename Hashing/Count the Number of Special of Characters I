class Solution {
    public int numberOfSpecialChars(String word) {
        int count=0;
        HashMap<Character,Integer> h=new HashMap<>();
        for(int i=0;i<word.length();i++){
            char c=word.charAt(i);
            if(Character.isUpperCase(c)){
                h.put(c,h.getOrDefault(c,0)+1);
            }
        }
        for(int i=0;i<word.length();i++){
            char c=word.charAt(i);
            if(Character.isLowerCase(c)){
                char ch=Character.toUpperCase(c);
                if(h.containsKey(ch)&&h.get(ch)>0){
                    count++;
                    h.put(ch,0);
                }
            }
        }
        return count;
    }
}



Example 1:

Input: word = "aaAbcBC"

Output: 3

Explanation:

The special characters in word are 'a', 'b', and 'c'.

Example 2:

Input: word = "abc"

Output: 0

Explanation:

No character in word appears in uppercase.

Example 3:

Input: word = "abBCab"

Output: 1

Explanation:

The only special character in word is 'b'.

