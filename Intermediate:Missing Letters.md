```
function fearNotLetter(str) {
  
  //1- Create an array with all letters 
  var allLetters = ["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","w","x","y","z"];
  
  //2- Split the string 
  var splitStr = str.split("");
  
  
 //3- Loop througgh the splited string 
  for (var i = 0; i < splitStr.length; i ++){
    
    //4- Check if the first letters are equal
    if(allLetters[0] === splitStr[0]){
      
         //5- create an empty array
         var n = [];
         //6- second for loop through the all  letters array
         for( var j = 0 ; j <allLetters.length ; j++){
           
           //7- if not eqaul push it to the array
             if(allLetters[j] !== splitStr[j]){
               
                  n.push(allLetters[j]);
                }
          }
      
          //return the first index of the array 
          return n[0] ;

     }else{
           //if the first index of both arrays are not equal return undefined
           return undefined;
           }
   
  }//END of first for loop 
  
  
}

fearNotLetter("bce");

```

#Strategy :

```

/*

Strategy:

1- Create an array with all letters to able to compare it with the string 

2- Split the string so it becomes an array 

3- For loop through the splited string 


4- Check if the first index in the all letters array is equal to the first index in the splited string array 


5- Create an empty array to capture the missing letters 

6- Second for loop to go through all letters array 

7- if they allLetters "letter" is not in the splitedString array , it will push to the n array 

8- return the array "n", for the purpose of this problem, we ONLY need the first index , so n[0] , otherwise; 

the array should return all the missing letters

9- if the first index of the arrays are not equal return undefined


*/
```

![Log](https://s10.postimg.org/mwc9k3u61/missing.jpg)
