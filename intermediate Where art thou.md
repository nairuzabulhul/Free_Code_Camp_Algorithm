```
function whatIsInAName(collection, source) {

  //filter through the array of objects
   var arrObject = collection.filter(function(item){
    
   //loop through the source keys
   for (var i in source){
       // if the source is NOT equal to the item return false, else return true
      if(source[i] !== item[i]){
          return false;
       }
   }
     return true;
  });

  //if it is true, return the array of objects
  return arrObject;
}
                                    
whatIsInAName([{ first: "Romeo", last: "Montague" }, { first: "Mercutio", last: null }, { first: "Tybalt", last: "Capulet" }], { last: "Capulet" });

```

## Strategy :

1- Filter the array of objects

2- For loop through the source keys 

3- if the value of source is not equal the value of the object in the array

Source value =  source[i]
Object value = item[i]

4- if the source[i] is not equal to item[i] return false

5- else return true

6- if it is true, return the array of objects


![Log](https://s4.postimg.org/kof9ar4q5/who.jpg)
