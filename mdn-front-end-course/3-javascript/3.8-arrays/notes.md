# Arrays

---

- Source : https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays

### What is an array? 

- Arrays are generally described as "list-like objects"; they are basically single objects that contain multiple values stored in a list. Array objects can be stored in variables and dealt with in much the same way as any other type of value, the difference being that we can access each value inside the list individually, and do super useful and efficient things with the list, like loop through it and do the same thing to every value. Maybe we've got a series of product items and their prices stored in an array, and we want to loop through them all and print them out on an invoice, while totaling all the prices together and printing out the total price at the bottom.

- If we didn't have arrays, we'd have to store every item in a separate variable, then call the code that does the printing and adding separately for each item. This would be much longer to write out, less efficient, and more error-prone. If we had 10 items to add to the invoice it would already be annoying, but what about 100 items, or 1000? We'll return to this example later on in the article.

### Creating arrays

Arrays consist of square brackets and items that are separated by commas.

- const shopping = ['bread', 'milk', 'cheese', 'hummus', 'noodles'];

- In the above example, each item is a string, but in an array we can store various data types — strings, numbers, objects, and even other arrays. We can also mix data types in a single array — we do not have to limit ourselves to storing only numbers in one array, and in another only strings. 

- const sequence = [1, 1, 2, 3, 5, 8, 13];
  
- const random = ['tree', 795, [0, 1, 2]];

### Finding the length of an array {.length}

- You can find out the length of an array (how many items are in it) in exactly the same way as you find out the length (in characters) of a string — by using the length property. 

### Accessing and modifying array items

- Items in an array are numbered, starting from zero. This number is called the item's index. So the first item has index 0, the second has index 1, and so on. You can access individual items in the array using bracket notation and supplying the item's index, in the same way that you accessed the letters in a string.

- You can also modify an item in an array by giving a single array item a new value. Try this: 

- shopping[0] = 'tahini';

- Note that an array inside an array is called a multidimensional array. You can access an item inside an array that is itself inside another array by chaining two sets of square brackets together. For example, to access one of the items inside the array that is the third item inside the random array (see previous section).

- const random = ['tree', 795, [0, 1, 2]];
  
- random[2][2]; // Prints 2

### Finding items in an array {indexOF()}

This is fine if you know the index of an item, but what if you don't? You can find the index of a particular item using the indexOf() method. This takes an item as an argument and returns the index, or -1 if the item was not found in the array.

- const birds = ['Parrot', 'Falcon', 'Owl'];

- console.log(birds.indexOf('Owl'));   //  2

- console.log(birds.indexOf('Rabbit')); // -1

### Adding items {push() END, unshift() START}

- To add one or more items to the end of an array we can use push(). Note that you need to include one or more items that you want to add to the end of your array.

- const cities = ['Manchester', 'Liverpool'];

- cities.push('Cardiff');

- console.log(cities);  // [ "Manchester", "Liverpool", "Cardiff" ]

- cities.push('Bradford', 'Brighton');

- console.log(cities);  // [ "Manchester", "Liverpool", "Cardiff", "Bradford", "Brighton" ]

- The new length of the array is returned when the method call completes. If you wanted to store the new array length in a variable.

- const cities = ['Manchester', 'Liverpool'];

- const newLength = cities.push('Bristol');

- console.log(cities);     // [ "Manchester", "Liverpool", "Bristol" ]

- console.log(newLength);  // 3

- To add an item to the start of the array, use unshift():

- const cities = ['Manchester', 'Liverpool'];

- cities.unshift('Edinburgh');

- console.log(cities);     // [ "Edinburgh", "Manchester", "Liverpool" ]

### Removing items {pop() END, shift() START, splice() INDEX};

#### To remove the last item from the array, use pop()

- const cities = ['Manchester', 'Liverpool'];

- cities.pop();

- console.log(cities);     // [ "Manchester" ]

- The pop() method returns the item that was removed. To save that item in a new variable, you could
  do this:
  
- const cities = ['Manchester', 'Liverpool'];

- const removedCity = cities.pop();

- console.log(removedCity);   // "Liverpool"

#### To remove the first item from an array, use shift()

- const cities = ['Manchester', 'Liverpool'];

- cities.shift();

- console.log(cities);     // [ "Liverpool" ]

#### If you know the index of an item, you can remove it from the array using splice()

- const cities = ['Manchester', 'Liverpool', 'Edinburgh', 'Carlisle'];

- const index = cities.indexOf('Liverpool');
  if (index !== -1) {
  cities.splice(index, 1);
}

- console.log(cities);     // [ "Manchester", "Edinburgh", "Carlisle" ]

- In this call to splice(), the first argument says where to start removing items, and the second argument says how many items should be removed. So you can remove more than one item:

- const cities = ['Manchester', 'Liverpool', 'Edinburgh', 'Carlisle'];

- const index = cities.indexOf('Liverpool');
  if (index !== -1) {
  cities.splice(index, 2);
}

- console.log(cities);     // [ "Manchester", "Carlisle" ]

### Accessing every item {for..of, map()}

- Very often you will want to access every item in the array. You can do this using the for...of statement:

- const birds = ['Parrot', 'Falcon', 'Owl'];

- for (const bird of birds) {
  console.log(bird);
}

- Sometimes you will want to do the same thing to each item in an array, leaving you with an array containing the changed items. You can do this using map(). The code below takes an array of numbers and doubles each number:

- function double(number) {
  return number * 2;
}

- const numbers = [5, 2, 7, 6];

- const doubled = numbers.map(double);

- console.log(doubled);  // [ 10, 4, 14, 12 ]

- We give a function to the map(), and map() calls the function once for each item in the array, passing in the item. It then adds the return value from each function call to a new array, and finally returns the new array.

- Sometimes you'll want to create a new array containing only the items in the original array that match some test. You can do that using filter(). The code below takes an array of strings and returns an array containing just the strings that are greater than 8 characters long:

- function isLong(city) {
  return city.length > 8;
}

- const cities = ['London', 'Liverpool', 'Totnes', 'Edinburgh'];

- const longer = cities.filter(isLong);

- console.log(longer);  // [ "Liverpool", "Edinburgh" ]






