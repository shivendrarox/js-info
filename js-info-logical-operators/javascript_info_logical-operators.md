**White Board Notes**
![Logical Operators](https://github.com/shivendrarox/js-info/blob/master/js-info-logical-operators/js-info-logical-operators.jpg)
___
## [Tasks](https://javascript.info/logical-operators#tasks)

### [What's the result of OR?](https://javascript.info/logical-operators#what-s-the-result-of-or)

[](https://javascript.info/task/alert-null-2-undefined)

importance: 5

What is the code below going to output?

`alert( null || 2 || undefined );`

**My Ans:**

> 2

**solution**

The answer is  `2`, that’s the first truthy value.

`alert( null || 2 || undefined );`

---
### [What's the result of OR'ed alerts?](https://javascript.info/logical-operators#what-s-the-result-of-or-ed-alerts)

[](https://javascript.info/task/alert-or)

importance: 3

What will the code below output?

`alert( alert(1) || 2 || alert(3) );`

**My Ans:**

> ~~1~~

**solution**

The answer: first  `1`, then  `2`.

`alert( alert(1) || 2 || alert(3) );`

The call to  `alert`  does not return a value. Or, in other words, it returns  `undefined`.

1.  The first OR  `||`  evaluates its left operand  `alert(1)`. That shows the first message with  `1`.
2.  The  `alert`  returns  `undefined`, so OR goes on to the second operand searching for a truthy value.
3.  The second operand  `2`  is truthy, so the execution is halted,  `2`  is returned and then shown by the outer alert.

There will be no  `3`, because the evaluation does not reach  `alert(3)`.

---
### [What is the result of AND?](https://javascript.info/logical-operators#what-is-the-result-of-and)

[](https://javascript.info/task/alert-1-null-2)

importance: 5

What is this code going to show?

`alert( 1 && null && 2 );`

**My Ans:**

> Null
>
**Solution:**

The answer:  `null`, because it’s the first falsy value from the list.

`alert( 1 && null && 2 );`

---

### [What is the result of AND'ed alerts?](https://javascript.info/logical-operators#what-is-the-result-of-and-ed-alerts)

[](https://javascript.info/task/alert-and)

importance: 3

What will this code show?

`alert( alert(1) && alert(2) );`

**My Ans:**

> 1 *Partially correct*

**solution:**
The answer:  `1`, and then  `undefined`.

`alert( alert(1) && alert(2) );`

The call to  `alert`  returns  `undefined`  (it just shows a message, so there’s no meaningful return).

Because of that,  `&&`  evaluates the left operand (outputs  `1`), and immediately stops, because  `undefined`  is a falsy value. And  `&&`  looks for a falsy value and returns it, so it’s done.

---
### [The result of OR AND OR](https://javascript.info/logical-operators#the-result-of-or-and-or)

[](https://javascript.info/task/alert-and-or)

importance: 5

What will the result be?

`alert( null || 2 && 3 || 4 );`
**My Ans:**

> 3

**solution**
The answer:  `3`.

`alert( null || 2 && 3 || 4 );`

The precedence of AND  `&&`  is higher than  `||`, so it executes first.

The result of  `2 && 3 = 3`, so the expression becomes:

`null || 3 || 4`

Now the result is the first truthy value:  `3`.

---
### [Check the range between](https://javascript.info/logical-operators#check-the-range-between)

[](https://javascript.info/task/check-if-in-range)

importance: 3

Write an  `if`  condition to check that  `age`  is between  `14`  and  `90`  inclusively.

“Inclusively” means that  `age`  can reach the edges  `14`  or  `90`.
**My Ans:**

    let age = prompt();
    
    if(age>=14 && age<=19){
        alert(true);
    }
---
### [Check the range outside](https://javascript.info/logical-operators#check-the-range-outside)

[](https://javascript.info/task/check-if-out-range)

importance: 3

Write an  `if`  condition to check that  `age`  is NOT between  `14`  and  `90`  inclusively.

Create two variants: the first one using NOT  `!`, the second one – without it.
**My Ans:**

    let age = prompt();
    
    if (!(age>=14 && age<=19)){
        alert(true);
    }

---
### [A question about "if"](https://javascript.info/logical-operators#a-question-about-if)

[](https://javascript.info/task/if-question)

importance: 5

Which of these  `alert`s are going to execute?

What will the results of the expressions be inside  `if(...)`?

`if (-1 || 0) alert( 'first' );
if (-1 && 0) alert( 'second' );
if (null || -1 && 1) alert( 'third' );`

**My Ans:**

> 'first'
> 'third
---
### [Check the login](https://javascript.info/logical-operators#check-the-login)

[](https://javascript.info/task/check-login)

importance: 3

Write the code which asks for a login with  `prompt`.

If the visitor enters  `"Admin"`, then  `prompt`  for a password, if the input is an empty line or  Esc  – show “Canceled”, if it’s another string – then show “I don’t know you”.

The password is checked as follows:

 1.   If it equals “TheMaster”, then show “Welcome!”,
 2.   Another string – show “Wrong password”,
 3.   For an empty string or cancelled input, show “Canceled”

**My Ans:**

    let user = prompt();
    
    if( user == "Admin"){
        let pass = prompt("enter a password");
        if (pass == "TheMaster"){
            alert("Welcome");
        }else if(pass == ""){
            alert("cancelled");
        }
        else{
            alert("Wrong Password");
        }
    }else if( user == ""){
        alert("Canceled");
    }else {
        alert("IDK You");
    }

>  1. Needs Improvement
>  2. Esc key press Not working as desired
>  3. used == instead of ===
>  4. forgot to use || and && at possible places

 
**Improved Answer**

    let user = prompt();
    
    if( user === "Admin"){
        let pass = prompt("enter a password");
        if (pass === "TheMaster"){
            alert("Welcome");
        }else if(pass === "" || pass === null){
            alert("cancelled");
        }
        else{
            alert("Wrong Password");
        }
    }else if( user === "" || user === null){
        alert("Canceled");
    }else {
        alert("IDK You");
    }
  
  **solution**

    let userName = prompt("Who's there?", '');
    
    if (userName === 'Admin') {
    
      let pass = prompt('Password?', '');
    
      if (pass === 'TheMaster') {
        alert( 'Welcome!' );
      } else if (pass === '' || pass === null) {
        alert( 'Canceled' );
      } else {
        alert( 'Wrong password' );
      }
    
    } else if (userName === '' || userName === null) {
      alert( 'Canceled' );
    } else {
      alert( "I don't know you" );
    }
---
