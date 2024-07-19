```
var lengthOfLongestSubstring = function(s) {
    let maxLength =0
    let left=0
    let right=0
    let length = s.length
    let strSet = new Set()

    while(right<length){

        if(!strSet.has(s[right])){
            strSet.add(s[right])
            right++
            maxLength = Math.max(maxLength,right-left)
        }else{
            strSet.delete(s[left])
            left++
        }
    }

    return maxLength
};

//Input: s = "abcabcbb"
//Output: 3
//Explanation: The answer is "abc", with the length of 3.
```
