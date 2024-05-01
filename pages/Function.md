- A Function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output.
- ## Function Declaration
  id:: 6631acf6-b39c-42d2-aa77-e49980697967
	- A **function definition** (also called a **function declaration**, or **function statement**) consists of the [`function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function) keyword, followed by:
		- The name of the function.
		- A list of parameters to the function, enclosed in parentheses and separated by commas.
		- The JavaScript statements that define the function, enclosed in curly braces, `{ /* … */ }`.
	- ```javascript
	  function showMessage() {
	    alert( 'Hello everyone!' );
	  }
	  ```
	- The `function` keyword goes first, then goes the *name of the function*, then a list of *parameters* between the parentheses (comma-separated, empty in the example above, we’ll see examples later) and finally the code of the function, also named “the function body”, between curly braces.
	- ```javascript
	  function name(parameter1, parameter2, ... parameterN) {
	   // body
	  }
	  ```
	- Our new function can be called by its name: `showMessage()`.
	- For instance:
	- ```javascript
	  function showMessage() {
	    alert( 'Hello everyone!' );
	  }
	  
	  showMessage();
	  showMessage();
	  ```
	- The call `showMessage()` executes the code of the function. Here we will see the message two times.
	- This example clearly demonstrates one of the main purposes of functions: to avoid code duplication.
	- If we ever need to change the message or the way it is shown, it’s 
	  enough to modify the code in one place: the function which outputs it.
- ## Function Expression
  id:: 6631b20d-7d63-4ed6-9aa0-ff8135abaec5
	- A `function` expression is very similar to, and has almost the same syntax as, a function declaration. The main difference between a `function` expression and a `function` declaration is the *function name*, which can be omitted in `function` expressions to create *anonymous* functions.
	- A `function` expression can be used as an IIFE (Immediately Invoked Function Expression) which runs as soon as it is defined. See also the chapter about [[Functions]] for more information.
	- ### Function expression hoisting
		- Function expressions in JavaScript are not hoisted, unlike function declarations. You can't use function expressions before you create them:
		- ```javascript
		  console.log(notHoisted); // undefined
		  // Even though the variable name is hoisted,
		  // the definition isn't. so it's undefined.
		  notHoisted(); // TypeError: notHoisted is not a function
		  
		  var notHoisted = function () {
		    console.log("bar");
		  };
		  ```
- ## Named Function Expression
  id:: 6631b3a0-3449-424c-9a47-71f8255bd875
	- If you want to refer to the current function inside the function body,  you need to create a named function expression. This name is then local  only to the function body (scope). This avoids using the deprecated `arguments.callee` property to call the function recursively.
	- ```javascript
	  const math = {
	    factit: function factorial(n) {
	      console.log(n);
	      if (n <= 1) {
	        return 1;
	      }
	      return n * factorial(n - 1);
	    },
	  };
	  
	  math.factit(3); //3;2;1;
	  
	  ```
	- If a function expression is named, the `name` property of the function is set to that name, instead of the implicit  name inferred from syntax (such as the variable the function is assigned to).
	- Unlike declarations, the name of the function expressions is read-only.
	- ```javascript
	  function foo() {
	    foo = 1;
	  }
	  foo();
	  console.log(foo); // 1
	  (function foo() {
	    foo = 1; // TypeError: Assignment to constant variable.
	  })();
	  
	  ```