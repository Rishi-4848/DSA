```
var findWordsContaining = function(words, x) {
     
     let output = []

    for(let index=0;index<words.length;index++){
        if(words[index].includes(x)){
            output.push(index)
        }
    }

    return output
};

//Input: words = ["leet","code"], x = "e"
//Output: [0,1]
//Explanation: "e" occurs in both words: "leet", and "code". Hence, we return indices 0 and 1.
```
