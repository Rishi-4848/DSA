```
var maxProfit = function(prices) {
    let minPrice = Infinity
    let maxProfit =0

    for(let index=0;index<prices.length;index++){
        if(prices[index]<minPrice){
            minPrice = prices[index]
        }else{
            let profit = prices[index] -minPrice

            if(profit>maxProfit){
                maxProfit = profit
            }
        }
    }

    return maxProfit
};



//Input: prices = [7,1,5,3,6,4]
//Output: 5
//Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
//Note that buying on day 2 and selling on day 1 is not allowed because you must buy before you sell.
```
