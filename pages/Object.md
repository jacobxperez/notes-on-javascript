- JavaScript is designed on a simple object-based paradigm. An object is a built-in data type for storing key-value pairs. Data inside objects are unordered, and the values can be of any type.
  title:: Object
- ## Object Literals
  id:: 6631948e-a741-4051-9e0e-aea120e4287a
	- Object initializers are also called *object literals*. "Object initializer" is consistent with the terminology used by C++. The syntax for an object using an object initializer is:
	- ```JavaScript
	  const person = {
	      getName: function () {
	          return 'Name is ' + this.firstName + ' ' + this.lastName
	      },
	  }
	  
	  const funnyGuy = Object.create(person)
	  funnyGuy.firstName = 'Conan'
	  funnyGuy.lastName = "O'Brian"
	  console.log(funnyGuy)
	  
	  const newGuy = Object.create(person)
	  newGuy.firstName = 'Jacob'
	  newGuy.lastName = 'Perez'
	  console.log(newGuy)
	  ```
- ## Object Factory
  id:: 663194c9-74c2-44ba-9981-e0ab3d0529a1
	- ```javascript
	  function createCircle(radius) {
	      return {
	          radius,
	          draw: function () {
	              console.log('draw')
	          },
	      }
	  }
	  ```
- ## Object Constructor
  id:: 66319502-69e7-4a69-85ef-639f6c93c46f
	- ```javascript
	  function Circle(radius) {
	      this.radius = radius
	      this.draw = function () {
	          console.log('draw')
	      }
	  }
	  
	  const another = new Circle(1)
	  ```