## Properties and values of a JavaScript object
	- A JavaScript object literal is enclosed with curly braces `{}`. Values are mapped to keys in the object with a colon `( : )`, and the key-value pairs are separated by commas.
	- All the keys are unique, but values are not.
	- Key-value pairs of an object are also referred to as properties.
	- ```javascript
	  const classOf2018 = {
	    students: 38,
	    year: 2018
	  }
	  ```
	- Properties of a JavaScript object can be accessed using the dot notation in this manner:
		- `object.propertyName`
	- Nested properties of an object can be accessed by chaining key names in the correct order.
	- ```javascript
	  const apple = {
	      color: 'Green',
	      price: {
	      bulk: '$3/kg',
	      smallQty: '$4/kg'
	    }
	  };
	  console.log(apple.color); // 'Green'
	  console.log(apple.price.bulk); // '$3/kg'
	  ```
- ## Accessing non-existent JavaScript properties
	- When trying to access a JavaScript object property that has not been defined yet, the value of undefined will be returned by default.
	- ```javascript
	  const classElection = {
	  	date: 'January 12'
	  };
	  
	  console.log(classElection.place); // undefined
	  ```
- ## Delete operator
	- Once an object is created in JavaScript, it is possible to remove properties from the object using the delete operator.
	- The delete keyword deletes both the value of the property and the property itself from the object.
	- The delete operator only works on properties, not on variables or functions.
	- ```javascript
	  const person = {
	    firstName: "Matilda",
	    age: 27,
	    hobby: "knitting",
	    goal: "learning JavaScript"
	  };
	  delete person.hobby; // or delete
	  person[hobby];
	  console.log(person);
	  
	  /*
	  {
	    firstName: "Matilda"
	    age: 27
	    goal: "learning JavaScript"
	  }
	  */
	  ```