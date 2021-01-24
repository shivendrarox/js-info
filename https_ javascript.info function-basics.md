## [Tasks](https://javascript.info/function-basics#tasks)

### [Is "else" required?](https://javascript.info/function-basics#is-else-required)

[](https://javascript.info/task/if-else-required)

importance: 4

The following function returns  `true`  if the parameter  `age`  is greater than  `18`.

Otherwise it asks for a confirmation and returns its result:

`function checkAge(age) {
  if (age > 18) {
    return true;
 _} else {
    // ...
    return confirm('Did parents allow you?');
  }_
}`

Will the function work differently if  `else`  is removed?

`function checkAge(age) {
  if (age > 18) {
    return true;
  }
 _// ...
  return confirm('Did parents allow you?');_
}`

Is there any difference in the behavior of these two variants?

**My Ans:**
```javascript
no, both will behave the same
```
---

### [Rewrite the function using '?' or '||'](https://javascript.info/function-basics#rewrite-the-function-using-or)

[](https://javascript.info/task/rewrite-function-question-or)

importance: 4

The following function returns  `true`  if the parameter  `age`  is greater than  `18`.

Otherwise it asks for a confirmation and returns its result.

`function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    return confirm('Did parents allow you?');
  }
}`

Rewrite it, to perform the same, but without  `if`, in a single line.

Make two variants of  `checkAge`:

1.  Using a question mark operator  `?`
2.  Using OR  `||`

**My Ans:**
```javascript
function checkAge(age) {
  return (age > 18)? true :  confirm('Did parents allow you?');
}
checkAge(19);
checkAge(5);
```
```javascript
function checkAge(age) {
  return (age > 18) || confirm('Did parents allow you?');
}
checkAge(19);
checkAge(5);
```
---

### [Function min(a, b)](https://javascript.info/function-basics#function-min-a-b)

[](https://javascript.info/task/min)

importance: 1

Write a function  `min(a,b)`  which returns the least of two numbers  `a`  and  `b`.

For instance:

`min(2, 5) == 2
min(3, -1) == -1
min(1, 1) == 1`

**My Ans:**
```javascript
function min(a,b){
    return (a>b)? b:a;
}
```
---

### [Function pow(x,n)](https://javascript.info/function-basics#function-pow-x-n)

[](https://javascript.info/task/pow)

importance: 4

Write a function  `pow(x,n)`  that returns  `x`  in power  `n`. Or, in other words, multiplies  `x`  by itself  `n`  times and returns the result.

`pow(3, 2) = 3 * 3 = 9
pow(3, 3) = 3 * 3 * 3 = 27
pow(1, 100) = 1 * 1 * ...* 1 = 1`

Create a web-page that prompts for  `x`  and  `n`, and then shows the result of  `pow(x,n)`.

[Run the demo](https://javascript.info/function-basics#)

P.S. In this task the function should support only natural values of  `n`: integers up from  `1`.

**My Ans:**
~~function pow(x=1,n=1){
    let total = 1;
    for (;n>=1;n--){
        total *= x
    }
    return total;
}
let x = prompt("enter the num");
let n = prompt("enter the power");
alert(pow(x,n));~~
> partialy correct
> no check for negative power :(

**My improved Ans:**
```javascript
function pow(x=1,n=1){
    let total = 1;
    for (;n>=1;n--){
        total *= x
    }
    return total;
}

let x = prompt("enter the num");
let n = prompt("enter the power");

if(n<1){
    alert(`Power ${n} is not supported, use a positive integer`);
}
else{
    alert(pow(x,n));
}
```

---
