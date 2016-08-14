```

function uniteUnique(arr) {
  var args = Array.prototype.slice.call(arguments);
  
  var newArr = [];
  
  //first loop
  for (var i = 0 ; i < args.length ; i ++){
    
    //second loop
    for (var j = 0 ; j < args[i].length ; j++){
      
      //push items to the array 
      newArr.push(args[i][j]);
    }
      
  }

  
 //Filter to remove the duplicates
  var newArr1 = newArr.filter(function(item, number){
     return newArr.indexOf(item) == number; 
  });
  
  
  return newArr1;
}


uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);

```

## Strategy 

1- Check how many argument are passing in the function using :

  Array.prototype.slice.call(arguments)

2- Create an empty arry to capture the output of the for loop


3- We need 2 for loops. First for loop goes through the whole array and second for loop plucks the items from the

second array and merge them into one whole array 

```
for (var i = 0 ; i < args.length ; i ++){
    
    for (var j = 0 ; j < args[i].length ; j++){
      
      newArr.push(args[i][j]);
    }
      //newArr.push(args[i]);
  }
  
  ```
 //result
 [1,3,2,5,2,1,4,2,1]
 
 
 4-filter the array to remove the duplicates 
 ```
 var newArr1 = newArr.filter(function(item, number){
     return newArr.indexOf(item) == number; 
   });
```
5- return newArr1


![Log] (https://s4.postimg.org/u67u4jr6l/sorted.jpg)
