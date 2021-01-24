## [Tasks](https://javascript.info/while-for#tasks)

### [Last loop value](https://javascript.info/while-for#last-loop-value)

[](https://javascript.info/task/loop-last-value)

importance: 3

What is the last value alerted by this code? Why?

    `let i = 3;
    
    while (i) {
      alert( i-- );
    }`

**My Ans**

> 1
---
### [Which values does the while loop show?](https://javascript.info/while-for#which-values-does-the-while-loop-show)

[](https://javascript.info/task/which-value-while)

importance: 4

For every loop iteration, write down which value it outputs and then compare it with the solution.

Both loops  `alert`  the same values, or not?

1.  The prefix form  `++i`:
    
  

      `let i = 0;
        while (++i < 5) alert( i );`
    
2.  The postfix form  `i++`
    
    `let i = 0;
    while (i++ < 5) alert( i );`

**My Ans**

>  ~~No, the postfix version will start from 0 where the prefix version will start from 1~~

**Improved ans:**

> NO, as the postfix version will alert 5 at counter = 4
---
### [Which values get shown by the "for" loop?](https://javascript.info/while-for#which-values-get-shown-by-the-for-loop)

[](https://javascript.info/task/which-value-for)

importance: 4

For each loop write down which values it is going to show. Then compare with the answer.

Both loops  `alert`  same values or not?

1.  The postfix form:
    
    `for (let i = 0; i < 5; i++) alert( i );`
    
2.  The prefix form:
    
    `for (let i = 0; i < 5; ++i) alert( i );`

**My Ans:**
>0 to 4 in both the cases
---
### [Output even numbers in the loop](https://javascript.info/while-for#output-even-numbers-in-the-loop)

[](https://javascript.info/task/for-even)

importance: 5

Use the  `for`  loop to output even numbers from  `2`  to  `10`.
```javascript
for(let i = 1; i<=10;i++){
    if( i % 2 === 0) alert(i);
}
```
---
### [Replace "for" with "while"](https://javascript.info/while-for#replace-for-with-while)

[](https://javascript.info/task/replace-for-while)

importance: 5

Rewrite the code changing the  `for`  loop to  `while`  without altering its behavior (the output should stay same).

```
for (let i = 0; i < 3; i++) {
  alert( `number ${i}!` );
}
```
**My Ans**
```javascript
let i=0;
while(i<3){
    alert(`number ${i}!`);
    i++;
}
```
---
### [Repeat until the input is correct](https://javascript.info/while-for#repeat-until-the-input-is-correct)

[](https://javascript.info/task/repeat-until-correct)

importance: 5

Write a loop which prompts for a number greater than  `100`. If the visitor enters another number – ask them to input again.

The loop must ask for a number until either the visitor enters a number greater than  `100`  or cancels the input/enters an empty line.

Here we can assume that the visitor only inputs numbers. There’s no need to implement a special handling for a non-numeric input in this task.

***My Ans:***
```javascript
for(;;){
  let num =  prompt("Enter a num>100",0);
    if (num > 100 || num == null){
        break;
    }else{
        continue;
    }
}
```
**Solution:**
```javascript
let num;

do {
  num = prompt("Enter a number greater than 100?", 0);
} while (num <= 100 && num);
```

The loop  `do..while`  repeats while both checks are truthy:

1.  The check for  `num <= 100`  – that is, the entered value is still not greater than  `100`.
2.  The check  `&& num`  is false when  `num`  is  `null`  or an empty string. Then the  `while`  loop stops too.

P.S. If  `num`  is  `null`  then  `num <= 100`  is  `true`, so without the 2nd check the loop wouldn’t stop if the user clicks CANCEL. Both checks are required.

----
### [Output prime numbers](https://javascript.info/while-for#output-prime-numbers)

[](https://javascript.info/task/list-primes)

importance: 3

An integer number greater than  `1`  is called a  [prime](https://en.wikipedia.org/wiki/Prime_number)  if it cannot be divided without a remainder by anything except  `1`  and itself.

In other words,  `n > 1`  is a prime if it can’t be evenly divided by anything except  `1`  and  `n`.

For example,  `5`  is a prime, because it cannot be divided without a remainder by  `2`,  `3`  and  `4`.

**Write the code which outputs prime numbers in the interval from  `2`  to  `n`.**

For  `n = 10`  the result will be  `2,3,5,7`.

P.S. The code should work for any  `n`, not be hard-tuned for any fixed value.
***My Ans:***
```javascript
let num = +prompt();

for (let c = 2;c<num;c++){
    let isPrime = true;
    for(let divs = 2 ; divs < c ;divs++){
        if(c%divs == 0 && c != divs){
            isPrime = false;
        }
    }
    if (isPrime){
        alert(c);
    }
}
```
----
