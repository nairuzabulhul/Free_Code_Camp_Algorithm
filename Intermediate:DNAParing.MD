
```
function pairElement(str) {
  
 //1- split the string 
  splitStr = str.split("");
 
  //2-Create an empyt array to be the large array that will contain all the sun arrays
  var dnaArr = [];
  
  //3- for loop through the string length 
  for (var i = 0 ; i < splitStr.length; i++){
    
    //4- create an inner array to each item of the string
    var subArray = [];
    
    //5- push the element to the subArray
     subArray.push(splitStr[i]);
    
    //6- Check the subArray index[0] 
    if(subArray[0] === "A"){
      
       subArray[1] = "T"; //if the first index is A , the second would be T
      
    }if(subArray[0] === "T"){
       
        subArray[1] ="A";
      
    }if(subArray[0] === "C"){
      
       subArray[1] ="G";
      
    }if(subArray[0] === "G"){
      
      subArray[1] = "C";
    }
    
    //7- Once done checking, push the subarrays to the larger array "strArray"
     dnaArr.push(subArray);
   }
  
  return dnaArr;
}

pairElement("ATCGA");

```


##Strategy:
1- Split the string using split method,

2- for loop through the string length 

3- creat an inner array inside the forloop 

4- push every element fromt the string to the array

5- Use if statement to check for the fist index of the array

6- After checking the inner array index, push to the larger array

7- return the array


![Log](https://s10.postimg.org/rf17uacx5/dns.jpg)
