# Basic math in JavaScript — numbers and operators

---

- Source: https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math

#### Everybody loves Math

Okay, maybe not. Some of us like math, some of us have hated math ever since we had to learn multiplication tables and long division in school, and some of us sit somewhere in between the two. But none of us can deny that math is a fundamental part of life that we can't get very far without. This is especially true when we are learning to program JavaScript (or any other language for that matter) — so much of what we do relies on processing numerical data, calculating new values, and so on, that you won't be surprised to learn that JavaScript has a full-featured set of math functions available.

This article discusses only the basic parts that you need to know now.

##### Types of numbers

In programming, even the humble decimal number system that we all know so well is more complicated than you might think. We use different terms to describe different types of decimal numbers, for example:

  -  **Integers** are floating-point numbers without a fraction. They can either be positive or negative, e.g. 10, 400, or -5.
  -  **Floating point numbers (floats)** have decimal points and decimal places, for example 12.5, and 56.7786543.
  -  **Doubles** are a specific type of floating point number that have greater precision than standard floating point numbers (meaning that they are accurate to a greater number of decimal places).

We even have different types of number systems! **Decimal** is base 10 (meaning it uses 0–9 in each column), but we also have things like:

  -  **Binary** — The lowest level language of computers; 0s and 1s.
  -  **Octal** — Base 8, uses 0–7 in each column.
  -  **Hexadecimal** — Base 16, uses 0–9 and then a–f in each column. You may have encountered these numbers before when setting colors in CSS.

**Before you start to get worried about your brain melting, stop right there!** For a start, we are just going to stick to decimal numbers throughout this course; you'll rarely come across a need to start thinking about other types, if ever.

The second bit of good news is that unlike some other programming languages, JavaScript only has one data type for numbers, both integers and decimals — you guessed it, <code>Number</code>. This means that whatever type of numbers you are dealing with in JavaScript, you handle them in exactly the same way.

##### It's all numbers to me

First of all, let's declare a couple of variables and initialize them with an integer and a float, respectively, then type the variable names back in to check that everything is in order:

<code>const myInt = 5;</code>

<code>const myFloat = 6.667;</code>

<code>myInt; // 5</code>

<code>myFloat; // 6.667</code>

Number values are typed in without quote marks — try declaring and initializing a couple more variables containing numbers before you move on.

Now let's check that both our original variables are of the same datatype. There is an operator called <code>typeof</code> in JavaScript that does this. Enter the below two lines as shown:

<code>typeof myInt; // "number"</code>

<code>typeof myFloat; // "number"</code>

You should get "number" returned in both cases — this makes things a lot easier for us than if different numbers had different data types, and we had to deal with them in different ways. Phew!

##### Useful Number methods

The Number object, an instance of which represents all standard numbers you'll use in your JavaScript, has a number of useful methods available on it for you to manipulate numbers. We don't cover these in detail in this article because we wanted to keep it as a simple introduction and only cover the real basic essentials for now; however, once you've read through this module a couple of times it is worth going to the object reference pages and learning more about what's available.

##### Converting to number data Types

Sometimes you might end up with a number that is stored as a string type, which makes it difficult to perform calculations with it. This most commonly happens when data is entered into a form input, and the input type is text. There is a way to solve this problem — passing the string value into the <code>Number()</code> constructor to return a number version of the same value.

#### Arithmetic operators

Arithmetic operators are the basic operators that we use to do sums in JavaScript.

##### Operator precedence

Assuming that num2 holds the value 50 and num1 holds the value 10:

<code>num2 + num1 / 8 + 2;</code>

As a human being, you may read this as "50 plus 10 equals 60", then "8 plus 2 equals 10", and finally "60 divided by 10 equals 6".

But the browser does "10 divided by 8 equals 1.25", then "50 plus 1.25 plus 2 equals 53.25".

This is because of **operator precedence** — some operators are applied before others when calculating the result of a calculation (referred to as an ***expression***, in programming). Operator precedence in JavaScript is the same as is taught in math classes in school — **multiply and divide are always done first, then add and subtract (the calculation is always evaluated from left to right).**

If you want to override operator precedence, you can put parentheses round the parts that you want to be explicitly dealt with first. So to get a result of 6, we could do this:

<code>(num2 + num1) / (8 + 2);</code>

#### Increment and decrement operators

Sometimes you'll want to repeatedly add or subtract one to or from a numeric variable value. This can be conveniently done using the increment (++) and decrement (--) operators. We used ++ in our "Guess the number" game back in our first splash into JavaScript article, when we added 1 to our guessCount variable to keep track of how many guesses the user has left after each turn.

<code>guessCount++;</code>

#### Assignment operators

Assignment operators are operators that assign a value to a variable. We have already used the most basic one, =, loads of times — it assigns the variable on the left the value stated on the right:

<code>let x = 3; // x contains the value 3</code>

<code>let y = 4; // y contains the value 4</code>

<code>x = y; // x now contains the same value y contains, 4</code>

But there are some more complex types, which provide useful shortcuts to keep your code neater and more efficient.

Ex:

- ***+=***
  - <code>x += 4;</code>, shortcut for ***x = x + 4***

- ***-=***
  - <code>x -= 3;</code>, shortcut for ***x = x - 3***

#### Comparison operators

Sometimes we will want to run true/false tests, then act accordingly depending on the result of that test — to do this we use **comparison operators**.

Ex:

- **===**

  - Strict equality, tests whether left and right values are equal to one another

- **!==**

  - Strict-non-equality, tests whether the left and right values are **not** identical to one another

- **<**, **>**, **<=**, **>=**

  - Less than, Greater than, less than or equal to, greater than or equal to

If you try entering some of these values in a console, you'll see that they all return true/false values — those booleans we mentioned in the last article. These are very useful, as they allow us to make decisions in our code, and they are used every time we want to make a choice of some kind. For example, booleans can be used to:

  -  Display the correct text label on a button depending on whether a feature is turned on or off

  -  Display a game over message if a game is over or a victory message if the game has been won

  -  Display the correct seasonal greeting depending what holiday season it is

  -  Zoom a map in or out depending on what zoom level is selected
