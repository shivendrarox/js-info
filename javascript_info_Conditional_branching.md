# Exercise

### [if (a string with zero)](https://javascript.info/ifelse#if-a-string-with-zero)

[](https://javascript.info/task/if-zero-string)

importance: 5

Will  `alert`  be shown?

    `if ("0") {
      alert( 'Hello' );
    }
**Answer**
Yes, because its a non empty string
___
### [The name of JavaScript](https://javascript.info/ifelse#the-name-of-javascript)

[](https://javascript.info/task/check-standard)

importance: 2

Using the  `if..else`  construct, write the code which asks: ‘What is the “official” name of JavaScript?’

If the visitor enters “ECMAScript”, then output “Right!”, otherwise – output: “Didn’t know? ECMAScript!”
**Answer**

    let answer = prompt("What is the official name of JavaScript","Your answer here");
    if(answer == "ECMAScript"){
        alert("Right");
    }else{
    alert(`You dont know "ECMAScript"!`);
    }
___
### [Show the sign](https://javascript.info/ifelse#show-the-sign)

[](https://javascript.info/task/sign)

importance: 2

Using  `if..else`, write the code which gets a number via  `prompt`  and then shows in  `alert`:

-   `1`, if the value is greater than zero,
-   `-1`, if less than zero,
-   `0`, if equals zero.

In this task we assume that the input is always a number.
**Answer**

    let num = prompt("Enter a number");
    
    if ( num > 0){
        alert(1);
    }else if(num < 0 ){
        alert(-1);
    }else{
    alert(0);
    }
___

### [Rewrite 'if' into '?'](https://javascript.info/ifelse#rewrite-if-into)

[](https://javascript.info/task/rewrite-if-question)

importance: 5

Rewrite this  `if`  using the conditional operator  `'?'`:

    let result;
    
    if (a + b < 4) {
      result = 'Below';
    } else {
      result = 'Over';
    }

**Ans**

    let result;
    let a=-1;
    let b= 4;
    
    (a+b<4)?result = "Below" : result = "Over";
___
### [Rewrite 'if..else' into '?'](https://javascript.info/ifelse#rewrite-if-else-into)

[](https://javascript.info/task/rewrite-if-else-question)

importance: 5

Rewrite  `if..else`  using multiple ternary operators  `'?'`.

For readability, it’s recommended to split the code into multiple lines.


    let message;
    
    if (login == 'Employee') {
      message = 'Hello';
    } else if (login == 'Director') {
      message = 'Greetings';
    } else if (login == '') {
      message = 'No login';
    } else {
      message = '';
    }
**Ans:**

    let message;
    let login = prompt();
     (login == 'Employee')? message = 'Hello':
     (login == 'Director')? message = 'Greetings':
     (login == '')? message = 'No login':message = '';

