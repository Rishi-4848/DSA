```
var moveZeroes = function(nums) {

    let pointer =0
   
   for(let index=0;index<nums.length;index++){
     if(nums[index] !==0){
       nums[pointer] = nums[index]
       pointer++
     }
   }

   for(let i =pointer;i<nums.length;i++){
    nums[i] =0
   }

    return nums
};

//Input: nums = [0,1,0,3,12]
//Output: [1,3,12,0,0]

```
