# practice

//flat Array

const flatArray = (arr) => {
    return arr.reduce((acc,cur)=>{
      return  Array.isArray(cur) ? acc.concat(flatArray(cur)) : acc.concat(cur)
    },[])
    
}
console.log(flatArray([1,[2,4,[5]]]))

//Palindrome number & string 

const pal = (str) =>{
    str = str.toString();
    let rev ="";
    for(i = str.length - 1; i >= 0; i--){
        // console.log(i)
        rev += str[i]
    }
    if(str == rev){
        return 'Palindrome'
    }else {
        return 'not Palindrome'
    }
}

console.log(pal(121))



//largest number from array

const largestNum = (num) =>{
    let largest = 0;
    for(i=0; i < num.length ; i++){
        if(largest < num[i]){
            largest = num[i]
        }
    }
    return largest
}


console.log(largestNum([1,2.4,09,800,23,90,955]))







