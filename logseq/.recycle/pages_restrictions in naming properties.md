- JavaScript object key names must adhere to some restrictions to be valid. Key names must either be strings or valid identifier or variable names (i.e. special characters such as - are not allowed in key names that are not strings)
- ```JavaScript
  // Example of invalid key names
  const trainSchedule = {
    platform num: 10, // Invalid because of the space between words.
    40 - 10 + 2: 30, // Expressions cannot be keys.
    +compartment: 'C' // The use of a + sign is invalid unless it is enclosed in quotations.
  }
  ```