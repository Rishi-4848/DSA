```
var threeSum = function(nums) {
    
    nums.sort((a,b)=>a-b)

    let result = []

    for(let index=0;index<nums.length-2;index++){

        if(index>0 && nums[index]== nums[index-1]){
            continue
        }

        let left = index+1
        let right= nums.length-1

        while(left<right){
            let sum = nums[index]+nums[left]+nums[right]

            if(sum===0){
                result.push([nums[index],nums[left],nums[right]])

                while(left<right && nums[left]==nums[left+1]){
                    left++
                }

                while(left<right && nums[right] == nums[right-1]){
                    right--
                }

                left++
                right--
            }else if(sum<0){
                left++
            }else{
                right--
            }
        }
    }

    return result
};

//Input: nums = [-1,0,1,2,-1,-4]
//Output: [[-1,-1,2],[-1,0,1]]
```
