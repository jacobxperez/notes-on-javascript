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