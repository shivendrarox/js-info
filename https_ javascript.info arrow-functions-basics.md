# Arrow functions, the basics

### [Rewrite with arrow functions](https://javascript.info/arrow-functions-basics#rewrite-with-arrow-functions)

[](https://javascript.info/task/rewrite-arrow)

Replace Function Expressions with arrow functions in the code below:

    `function ask(question, yes, no) {
      if (confirm(question)) yes()
      else no();
    }
    
    ask(
      "Do you agree?",
      function() { alert("You agreed."); },
      function() { alert("You canceled the execution."); }
    );`

**My ans:**

```javascript
function ask(question, yes, no){
  if (confirm(question)) yes()
  else no();
}

ask(
  "Do you agree?",
  () => alert("You agreed."),
  () =>  alert("You canceled the execution.")
);
```
