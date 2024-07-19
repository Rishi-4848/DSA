```
var groupAnagrams = function(strs) {
    
    let obj = {}

    for(let index=0;index<strs.length;index++){
        let value = strs[index].split("").sort().join("")

        if(obj[value] === undefined){
            obj[value] = [strs[index]]
        }else{
            obj[value].push(strs[index])
        }
    }

    let result = []

    Object.values(obj).map((value)=>{
        result.push(value)
    })

    return result
};



//Input
//strs =["eat","tea","tan","ate","nat","bat"]

//Output
//[["eat","tea","ate"],["tan","nat"],["bat"]]
```
