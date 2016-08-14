```
function convertHTML(str) {
//Regex
  var regexStr = /[>"'&<]/;
  
  //test if the sting contains one of the regex symbols
  if(regexStr.test(str)){
    
    var newArr = []; //new array to contain all the separated letters
    
    var newStr = ""; //empty string 
    
    //for loop through the string to separate the letters
     for(var i = 0; i < str.length ; i++){
        newArr.push(str[i]);  //push the lettes to the new array
      }
    
    //seconf for loop through the new array to check the sub elements of the array 
    for(var n = 0; n < newArr.length; n ++){   
       //Ampersand
        if(newArr[n] === "&"){
         newArr[n] ="&amp;"; // replace the letter with HTML entitiy
        } 
        
       //Single Quotes
        if(newArr[n] === "'"){
          newArr[n] ="&apos;"; //replace the letter with HTML entitiy
        } 
        
       //Double Quotes
        if(newArr[n] === '"'){
          newArr[n] ="&quot;"; //replace the letter with HTML entitiy
        } 
        
      //Less than sign
       if(newArr[n] === ">"){
          newArr[n] = "&gt;"; //replace the letter with HTML entitiy
        }
        
      //Greater than sign
        if(newArr[n] === "<"){
           newArr[n] = "&lt;"; //replace the letter with HTML entitiy
        }
      
       //After checking, add the replaces and non-repalced letters to the new empty string 
       newStr += newArr[n];    
    }
    
    //return the new string
    return newStr; 
  }
  
  //if the string does not contain anything elements from the regex return it as it is .
  return str;
}

convertHTML("abc");


```



## Statgey :

1- create a regex object with all the mentioned HTML entities

regex = /[<>"'&]/

note: the bracket here to help combine all of the sybomls togther in one regext object

2- Now we have to test the strig if it contains one of the regex symbols or not by using regex.test() function


 //if(regex.test(str)){
   return true; //return true if it contains a regex symbol 
     }
 return false;  //if it does not contain regex symbol


3- if it is true:

 - create a new array and new string 
 
 - for loop through the string and push to the array :
   this step will help you separate the letters
   
   ["m","&","t"];
   
  - for loop through the new Array and check if the items are equal to one of the regex symbol:
  
    if yes :
      repalce with the HTML entity and add to the new string 
    if No:
    
    add the 
   
    add to the new string
    
  - When done checking, return the new String  


4- if the string does not contain any of the regex symbol, return it as it is 


![Log](https://s4.postimg.org/cf6tfjr8t/html.jpg)
