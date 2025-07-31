# practice

//flat Array

const flatArray = (arr) => {
    return arr.reduce((acc,cur)=>{
      return  Array.isArray(cur) ? acc.concat(flatArray(cur)) : acc.concat(cur)
    },[])
    
}


console.log(flatArray([1,[2,4,[5]]]))

