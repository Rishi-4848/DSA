```
var topKFrequent = function(nums, k) {
    
    let numsMap = new Map()

    for(let index=0;index<nums.length;index++){
        if(numsMap.has(nums[index])){
            numsMap.set(nums[index], numsMap.get(nums[index])+1)
        }else{
            numsMap.set(nums[index],1)
        }
    }

    
    let newArr = Array.from(numsMap).sort(((a,b)=> b[1]-a[1]))

  console.log(newArr)

  let resultArr = []

  for(let pointer=0;pointer<k;pointer++){
     resultArr.push(newArr[pointer][0])
  }

  return resultArr
};

//Input: nums = [1,1,1,2,2,3], k = 2
//Output: [1,2]
```
