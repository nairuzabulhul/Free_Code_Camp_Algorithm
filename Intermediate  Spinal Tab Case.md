```
function spinalCase(str) {

  
  var regexUnderScore = /_/;
  var regexSpace = / /;
  var regex = /([a-z])([A-Z])/g;

  str = str.replace(regex, '$1 $2');

  
  if(regexUnderScore.test(str)){
    
      return str.replace(/_/g,"-").toLowerCase();
   } 
  
   if(regexSpace.test(str)){
     
      return str.replace(/ /g,"-").toLowerCase();
  
   }
  
}

spinalCase('AllThe-small Things');

```

## Strategy:


1- first thing add a space between the letters using replace('$1 $2')


2- check of the regex in the string using test function 

![Log](https://s3.postimg.org/aoz1ql7ab/spine.jpg)
