- Classes can have a constructor method. This is a special method that is called when the object is created (instantiated). Constructor methods are usually used to set initial values for the object.
- ```JavaScript
  class Song {
  	constructor(title, artist) {
        this.title = title;
        this.artist = artist;
  	}
  }
  
  const mySong = new Song('Bohemian
  Rhapsody', 'Queen');
  console.log(mySong.title);
  ```