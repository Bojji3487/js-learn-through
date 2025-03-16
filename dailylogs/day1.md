# Today I learnt

## 1. Hoisting

Basically Javascript has this feature. When we define a function using the _function_ keyword, the function automatically gets transported to the top of the codeblock. So even though we are defining/initializing it below a code, the interpreter will execute it first AND we can call it whenever we want.

This wouldn't happen if we use the arrow function since it uses a const/let/var keyword to define a func.

Interestingly when defining a variable using _var_ keyword, it also hoists the variable but it is initialized as...let's say

var a=undefined; ....Until it is given a value

## 2. Call(),apply(),bind()

Idk how useful they would be but bind sounds pretty useful.
<br>Basically these keywords enable preserving the _this_ keyword in a func. They also help in object passing, for example the apply keyword helps to pass both an object and an array as params. And the bind( ) enables to wrap a new function around an object.

## Array methods

Welp, talking not just about array but methods in js in general....They are one of the biggest reasons jaavscript is so accessible similar to Python. They are prebuilt functions defined to do specific work and come with the javascript package.
<br>

### 1.filter:

Woah. Being able to filter an array without 15 lines of for loop? Gimme that. <br>
eg. <pre> const arr=[
{name:"a" , price:200},
{name:"b" , price:30}];
const filteredList=arr.filter((elem)=>{
return elem.name=="a";
});
console.log(arr)
console.log(filteredList)

This returns:<pre>
[ { name: 'a', price: 200 }, { name: 'b', price: 30 } ]
[ { name: 'a', price: 200 } ]

</pre>
</pre>

### 2. Map

Makes a new array out of existing ones<br>

<pre>
const a=arr.map((arr,index)=>{
return arr.price;
})

console.log(a);</pre>

### 3. Find

Find an item<br>

<pre>
const valueFound=arr.find((arr)=>{
  return arr.price>30;
});

console.log(valueFound);</pre>

### 4. forEach

Iterate thru the whole array,helps in dom manipulation of nodelist<br>

<pre>
arr.forEach((arr)=>{
  console.log(arr.price)
});
</pre>

### 5. some and every

Basically && and || boolean methods<br>

<pre>
const checkprice=arr.some((arr)=>{
  return arr.price>=100;
});  //returns true

const checkprice=arr.every((arr)=>{
  return arr.price>=100;
});    //returns false
</pre>

### 6. includes

Iterate thru the whole array to find an element,boolean method<br>

<pre>
const prices = arr.map(item => item.price);
const flag=prices.includes(200);
const flag2=prices.includes(300);
console.log(flag); //true
console.log(flag2); //false
</pre>

## Closures

This basically means wrapping a function inside it's lexical environment. So whenever the function is called outside the parent. It still remembers the data outside it's scope.
<br>eg.

<pre>
 function outer(){
    let a=5;
    function inner(a){
      console.log(a);
    }
    inner(a);  //5
    a=78;
    inner(a);  //78
  }
  outer();
</pre>

## Types of functions

<pre>
Things learned:
1.  What is Function Statement ?
A.  A normal function that we create using Naming convention. & By this we can do the Hoisting.
      For Ex  -  function xyz(){
                            console.log("Function Statement");
                       }

2.  What is Function Expression ?
A.  When we assign a function into a variable that is Function Expression. & We can not do Hoisting by this becz it acts like variable.
      For Ex - var a = function(){
                            console.log("Function Expression");
                    }

3.  What is Anonymous Function ?
A.  A Function without the name is known as Anonymous Function. & It is used in a place where function are treated as value.
      For Ex - function(){
                     }

4.  What is Named Function Expression ?
A.  A function with a name is known as Named Function Expression.
      For Ex - var a = function xyx(){
                            console.log("Names Function Expression");
                     }

5.  Difference b/w Parameters and Arguments ?
A.  When we creating a function  & put some variabels in this ( ) that is our Parameters.
       For Ex - function ab( param1, param2 ){
                              console.log("
                      }
       & When we call this function & pass a variabel in this ( ) that is our Arguments
       For Ex - ab( 4, 5 );

6.  What is First Class Function Or First class citizens?
A.   The Ability of use function as value,
*     Can be passed as an Argument,
*     Can be executed inside a closured function &
*     Can be taken as return form.
       For Ex - var b = function(param){
                             return function xyz(){
                                     console.log(" F C F ");
                             }
                     } 

7. Function are heart of JS. They are called first class citizens or first class functions because they have the ability to be stored in the variables, passed as parameters and arguments. They can also be returned in the function.
