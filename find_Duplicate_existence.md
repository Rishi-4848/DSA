
#  checking duplicate existence
```
var containsDuplicate = function(nums) {
    
    // let sortedNums = nums.sort()

    // for(let index=0;index<sortedNums.length;index++){

    //     if(sortedNums[index]==sortedNums[index+1]){
           return true
     //   }
   //  }
  
  let numsSet = new Set()

    for(let index=0;index<nums.length;index++){
          
          if(numsSet.has(nums[index])){
            return true
          }else{
            numsSet.add(nums[index])
          }   
    }

    return false
};

```
