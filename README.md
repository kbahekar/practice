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



const duplicate = (arr) => {
  const seen = new Set();
  const duplicates = new Set();

  for (const num of arr) {
    if (seen.has(num)) {
      duplicates.add(num);
    } else {
      seen.add(num);
    }
  }

  return Array.from(duplicates);
};

console.log(duplicate([4, 2, 5, 6, 2]));




const countDuplicates = (arr) => {
  const map = {};
  for (const num of arr) {
    map[num] = (map[num] || 0) + 1;
  }
  return Object.entries(map).filter(([_, count]) => count > 1);
};

console.log(countDuplicates([4, 2, 5, 6, 2, 4])); 





//removeDuplicates
const removeDuplicates = (arr) => {
    let dup = [];
    for (let i = 0; i < arr.length; i++) {
        if (dup.indexOf(arr[i]) === -1) {
            dup.push(arr[i]);
        }
    }
    return dup;
}

console.log(removeDuplicates([1, 2, 4, 5, 6, 3, 2]));

















