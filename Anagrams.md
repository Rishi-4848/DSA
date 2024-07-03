```
var isAnagram = function(s, t) {
     
     let map1 = new Map()

     let sArr = s.split('')

     for(let index=0;index<sArr.length;index++){
       
       if(map1.has(sArr[index])){
            map1.set(sArr[index],map1.get(sArr[index])+1)
       }else{

        map1.set(sArr[index],1)
       }
     }

     for(let index2=0;index2<t.length;index2++){

        if(map1.has(t[index2])){

           map1.set(t[index2],map1.get(t[index2])-1)
        }else{
            return false
        }
     }

     console.log(map1)

     for(let index3 of map1.values()){

        if(index3 !== 0){
            return false
        }
     }

     return true
};

```
