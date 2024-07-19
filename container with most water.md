```
var maxArea = function(height) {
    
    let maxArea = 0
   let left =0
    let right = height.length-1

    while(left<right){

        let length = Math.min(height[left],height[right])
        let width = right-left
        let area = length*width

        if(area>maxArea){
            maxArea = area
        }
        if(height[left]<height[right]){
            left++
        }else{
            right--
        }
    }
    return maxArea
};

//Input: height = [1,8,6,2,5,4,8,3,7]
//Output: 49
//Explanation: The above vertical lines are represented by array [1,8,6,2,5,4,8,3,7]. In this case, the max area of water (blue section) the container can contain is 49.

```
