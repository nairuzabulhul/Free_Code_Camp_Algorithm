
```
function myReplace(str, before, after) {
  
 var newStr;
  
  # Check if the first index of before is lower case, if so replace before with after.
  # return the string
  
  if(before[0] === before[0].toLowerCase()){
    newStr = str.replace(before, after);
     return newStr;
  }  
  
  # else : capitalize the first letter, then replace before with after
  newWord = after.charAt(0).toUpperCase() + after.slice(1);
  newStr = str.replace(before,newWord);
  
  return newStr;
  
}
```
myReplace("Let us get back to more Coding", "Coding", "algorithms");


## Stratgey :

1- First check if the first index of "beofre" is a lowercase,

2- if so, Replace before with after , and return the newString

3- if the first index of before is not lowercase, capitalize the first letter of "after"

4- slice first index of "after" 

5-return newString

