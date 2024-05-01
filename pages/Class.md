- JavaScript supports the concept of classes as a syntax for creating objects. Classes specify the shared properties and methods that objects produced from the class will have.
- When an object is created based on the class, the new object is referred to as an instance of the class. New instances are created using the new keyword.
- The code sample shows a class that represents a Song:
	- ```JavaScript
	  class Song {
	    constructor() {
	      this.title;
	      this.author;
	    }
	    play() {
	    	console.log('Song playing!');
	    }
	  }
	  
	  const mySong = new Song();
	  mySong.play();
	  ```
	- A new object called `mySong` is created underneath and the `.play()` method on the class is called. The result would be the text Song playing! printed in the console.