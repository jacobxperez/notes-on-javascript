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
- Accessing non-existent JavaScript properties
	- When trying to access a JavaScript object property that has not been defined yet, the value of undefined will be returned by default.
	- ```javascript
	  const classElection = {
	  	date: 'January 12'
	  };
	  
	  console.log(classElection.place); // undefined
	  ```
-