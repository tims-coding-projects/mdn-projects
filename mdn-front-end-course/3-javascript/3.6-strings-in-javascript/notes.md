# Handling text — strings in JavaScript

---

- Source: https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings

#### The power of words

Words are very important to humans — they are a large part of how we communicate. Since the Web is a largely text-based medium designed to allow humans to communicate and share information, it is useful for us to have control over the words that appear on it. HTML provides structure and meaning to our text, CSS allows us to precisely style it, and JavaScript contains a number of features for manipulating strings, creating custom welcome messages and prompts, showing the right text labels when needed, sorting terms into the desired order, and much more.

Pretty much all of the programs we've shown you so far in the course have involved some string manipulation.

#### Strings - the basics

Just like we did with numbers, we are declaring a variable, initializing it with a string value, and then returning the value. The only difference here is that when writing a string, you need to surround the value with quotes.

##### Single quotes vs. double quotes

In JavaScript, you can choose single quotes or double quotes to wrap your strings in.

There is very little difference between the two, and which you use is down to personal preference. You should choose one and stick to it, however; differently quoted code can be confusing, especially if you use two different quotes on the same string!

However, you can't include the same quote mark inside the string if it's being used to contain them. The following will error, as it confuses the browser as to where the string ends.

##### Escaping characters in a string

Escaping characters means that we do something to them to make sure they are recognized as text, not part of the code. In JavaScript, we do this by putting a backslash just before the character.

Ex:

<code>const bigmouth = 'I\'ve got no right to take my place...';</code>

<code>console.log(bigmouth);</code>

#### Concatenating strings

Concatenate just means "join together". To join together strings in JavaScript you can use a different type of string, called a **template literal**.
A template literal looks just like a normal string, but instead of using single or double quote marks (' or "), you use backtick characters (`)

Ex:

<code>const greeting = `Hello`;</code>

This can work just like a normal string, except you can include variables in it, wrapped inside ${ } characters, and the variable's value will be inserted into the result:

<code>const name = 'Chris';</code>

<code>const greeting = `Hello, ${name}`;</code>

<code>console.log(greeting); // "Hello, Chris"</code>

You can use the same technique to join together two variables:

<code>const one = 'Hello, ';</code>

<code>const two = 'how are you?';</code>

<code>const joined = `${one}${two}`;</code>

<code>console.log(joined); // "Hello, how are you?"</code>

##### Concatenation in context

Let's have a look at concatenation being used in action:

<code><button>Press me</button></code>

<code>
const button = document.querySelector('button');

function greet() {
  const name = prompt('What is your name?');

  alert(`Hello ${name}, nice to see you!`);
}

button.addEventListener('click', greet);</code>

Here we're using the window.prompt() function, which asks the user to answer a question via a popup dialog box then stores the text they enter inside a given variable — in this case name. We then use the window.alert() function to display another popup containing a string which inserts the name into a generic greeting message.

##### Concatenation using "+"

You can also concatenate strings using the + operator

However, template literals usually give you more readable code

Ex:

<code>const greeting = "Hello";</code>

<code>const name = "Chris";</code>

<code>console.log(`${greeting}, ${name}`); // "Hello, Chris"</code>

#### Numbers vs. Strings
