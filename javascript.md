# **Javascript**
![javascript](https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/187_Js_logo_logos-128.png)

## **History of javascript**
1. **JavaScript** was devloped by **Brendan Eich in 1995**. Javascript language is created in just 10 days. It was originally named Mocha then livescript and later JvaScript.
2. earlier it used only in web browsers.for front-end part only.
3. Javascript language have some flow and drawback. because of they created this language in 10 days of time.
4. they never though javascript is use for arithmatic operation. because of that **javascript have tech debt.** .
    *  +(concat) => a + a ="aa"
    * == (normal check)
    * null
4. browsers
    * chrome
    * brave
    * mozilla firefox
    * safari   
## **Control Structure**
* if else
* for 
* switch case
* while
* do while 

## **Operators**
* **Arithmatic**
    * +, -, *, /, %, ++, --, += ,-=, == , ===.
* **Logical**
    * && , || , !
* **Bitwise**
    * | , & , ^
* **Ternary**
    * ?:
* **relational**
<p>&nbsp;</p>

# **javaScript Variable**
* javaScript is **dynamic** type language.
* Variable is like container which can hold any data(both primitive and non-primitive)
* there is 2 type of variable
    1. <span style="color:#6495ED"> **Primitive**(copy by value)</span>
        * string
        * number
        * boolean
        * undefine
        * null
        * symbol(es6)

        2.<span style="color:#6495ED"> **Non-Primitive**(copy by refrance)</span> (it is collection of primitive and non primitive data)
        * object 
        * array

 1. **var (ES5)** 
 2. **const, let (ES6)**

 | var | let | const |
| ------ | :------: | :-----: |
| can be redeclared | as per (es6) let can't be redeclared  | as per (es6) const can't be redeclared |
| can be re-initialize | can be re-initialize  | cann be re-initialize but non-primitive value can be updated |
| functional scope | laxical scope | laxical scope |
| hoisted | doesn't get hoisted | doesn't get hoisted |

### <span style="color:#6495ED">**Falsy value**</span>
* It is value that consider **false** when encounterd in boolean.
    * false
    * 0
    * undefine
    * NAN
    * " "

### <span style="color:#6495ED">**Truthy value**</span>
* It is value that consider **true** when encounterd in boolean
* other then falsy value all value are truthy value 
    * { }
    * [ ]
    * number
    * "string"
<p>&nbsp;</p>

### <span style="color:#6495ED">**Behaviour of variable**</span>
1. Act like container.
2. variable decleration get hoisted.
3. scope(global, local).
4. override.
<p>&nbsp;</p>

## Scope in javascript
* **functional scope** ( define using var keyword.)
    * A variable declared with in function have access with in that function only. we can't access that function outside the function

        ```
        var a=2;
          function hello(){
            var a= 10;         
            console.log(1. a)
           }
          hello();
            console.log(2.a)
        ```
        ```
        output: 1. 10
                2. 2
        ```
* in the above example var a=2 is global variable and after that we declare a function and inside function we are declaring another var a=10. 
this var a=10 has a functional scope .we can access the value var a=10 with in that function only. 
* **Lexical scope**
    * any block inside a functional scope. anything which is started with { } it is laxical scope.

    ```
    let a=5;
        if(a){          // lexical scope
          let b=9;
          let a= 10;
          console.log(a+b);
        }
    ```

## copy by value 

```

var a= 10;  // primitive 
var b=20;   // primitive    
b=a+30; 
console.log(b); 
console.log(a);
```
```
output: b=40
        a=10
```
<p>&nbsp;</p>

## copy by refrence
```
var stack = {       //non-primitive ( copy by refrence)
    node:1,
    php:1,
    go:1,
    es:[1,2]
}
var tech = stack;   // tech is pointing to stack
tech.go=10;
console.log("1",stack)
console.log("2",tech)
```
```
output: 1 { node: 1, php: 1, go: 10, es: [ 1, 2] }
        2 { node: 1, php: 1, go: 10, es: [ 1, 2] }
```
<p>&nbsp;</p>

# **Function**
1. Function is set of statment that perform a task 
    * syntax for **function decleration**
    ```
    function function_name(){ 
        // code
    }
    function_name();
    ```
     * syntax for **function assignment**
    ```
    var result=function function_name(){ 
        // code
    }
    result();
    ```
2. Function behave exactly same as variable. 
3. Behaviour of function
    * **hoisting**
    * **scope (Local , global)**
    * **ovrride**
    * **act as container**

**function is first-class citizen(it has all the privillage)**


## <span style="color:#6495ED">**Properties of Function**</span>   
<p>&nbsp;</p>

### <span style="color:#6495ED">**&nbsp;1. first-class citizen**</span>
* **function can assign to variable.**
* **function can return from another function.** 
* **function can pass as a parameter to function.**

### <span style="color:#6495ED">**&nbsp;2. Pure function**</span>
* pure function is function which do not get modified. and when we pass value it return the same value.
```
function add(a,b) {
    return a + b;
}
var one = 10;
var two = 50;
const result = add(one,two);
console.log(result);
```
### <span style="color:#6495ED">**&nbsp;3. Higher order function**</span>
* A function which take function as parameter or return a function

### <span style="color:#6495ED">**&nbsp;4. IIFE(Immediate invoked function expression)**</span>
* we use IIFE to create **private implementation** of function.
* It is also called SEF(self executable function)
```
(function(){
console.log("running......")
})();
```
```
output : running......
```
### <span style="color:#6495ED">**&nbsp;5. Inline Function**</span>
```
var outside= (function(next){    //function assignment
    console.log("print.....");

        function hello(value){
            console.log("called....");
            next && (typeof next === "function")&& next(value);
        }

        return hello;
})(function (value){
    console.log("printing value :",value)
});

outside(10);     // inline parameter
```
### Arrow Function

```
var a = () => {
    console.log("Arrow a")
}

b();
```
### Built in constructor 
* string
* number (avoid)
* boolean (avoid)
* object 
* math 
* array
* date
* function (avoid)
<p>&nbsp;</p>

### **Built in Function**
|built in function  | use for |
| ------ | :------: | 
|1. setTimeout(); |delay the code for specific time|
|2. setInterval(); | It run continuosly |
|3. clearInterval(); | it stop the interval .|
|4. parseInt(); | It convert into integer number. |
<p>&nbsp;</p>

### **Array built in method**
|built in method | use for |
| ------ | :------: | 
|1. push();  |Add value at ending of array  |
|2. pop(); | Remove last item. |
|3. indexof() | search the array for the specified item, and returns its position.|
|4. unshift(); | Add value at begining of array. |
|5. shift(); | Remove item from begining of array. |
|6. concat | Used merge two or more array. |
|7. map() | Create new array with result of calling a function for every array item. |
|8. includes() |  It same as index but output is true or false. |
|9. join() | joins all the items of an array into a string.
 |






