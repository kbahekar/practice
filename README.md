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



