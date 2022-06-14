# Storing the information you need — Variables

---

- Source: https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables


## What is a variable?

A variable is a container for a value, like a number we might use in a sum, or a string that we might use as part of a sentence.

  - Note: We say variables contain values. This is an important distinction to make. Variables aren't the values themselves; they are containers for values. You can think of them being like little cardboard boxes that you can store things in.

## Declaring a variables

To use a variable, you've first got to create it — more accurately, we call this declaring the variable. To do this, we type the keyword  <code>let</code> followed by the name you want to call your variable


## Initializing a variable

Once you've declared a variable, you can initialize it with a value. You do this by typing the variable name, followed by an equals sign (=), followed by the value you want to give it.

You can declare and initialize a variable at the same time, like this:

  - <code>let myVar = 'String';</code>

This is probably what you'll do most of the time, as it is quicker than doing the two actions on two separate lines.

## Updating a variables

Once a variable has been initialized with a value, you can change (or update) that value by giving it a different value.

 - <code>myVar = 'newString';</code>

#### An aside on variable naming rules

 You can call a variable pretty much anything you like, but there are limitations. Generally, you should stick to just using Latin characters (0-9, a-z, A-Z) and the underscore character.

     You shouldn't use other characters because they may cause errors or be hard to understand for an international audience.

     Don't use underscores at the start of variable names — this is used in certain JavaScript constructs to mean specific things, so may get confusing.

     Don't use numbers at the start of variables. This isn't allowed and causes an error.
     A safe convention to stick to is so-called "lower camel case", where you stick together multiple words, using lower case for the whole first word and then capitalize subsequent words. We've been using this for our variable names in the article so far.

     Make variable names intuitive, so they describe the data they contain. Don't just use single letters/numbers, or big long phrases.

     Variables are case sensitive — so myage is a different variable from myAge.

     One last point: you also need to avoid using JavaScript reserved words as your variable names — by this, we mean the words that make up the actual syntax of JavaScript!
     So, you can't use words like var, function, let, and for as variable names. Browsers recognize them as different code items, and so you'll get errors.

      - Good name examples:
              age
              myAge
              init
              initialColor
              finalOutputValue
              audio1
              audio2

      - Bad name examples:

              1
              a
              _12
              myage
              MYAGE
              var
              Document
              skjfndskjfnbdskjfb
              thisisareallylongvariablenameman

## Variable Types

#### Numbers

You can store numbers in variables, either whole numbers like 30 (also called integers) or decimal numbers like 2.456 (also called floats or floating point numbers). You don't need to declare variable types in JavaScript, unlike some other programming languages. When you give a variable a number value, you don't include quotes:

<code>let myNum = 215;</code>

#### Strings

Strings are pieces of text. When you give a variable a string value, you need to wrap it in single or double quote marks; otherwise, JavaScript tries to interpret it as another variable name.

<code>let ashSays = 'I woke up too late!!!!'</code>

#### Booleans

Booleans are true/false values — they can have two values, true or false. These are generally used to test a condition, after which code is run as appropriate. So for example, a simple case would be:

<code>let hulkSmash = true</code>

Whereas in reality it would be used more like this:

<code>let test = 10 < 5;</code>

#### Arrays

An array is a single object that contains multiple values enclosed in square brackets and separated by commas.

<code>let myNames = ['Alucard', 'Richter', 'Maria'];</code>

<code>let myNums = [5, 7, 13];</code>

#### Objects

In programming, an object is a structure of code that models a real-life object. You can have a simple object that represents a box and contains information about its width, length, and height, or you could have an object that represents a person, and contains data about their name, height, weight, what language they speak, how to say hello to them, and more.

<code>let summon = { name : 'Ifrit', element : 'Fire' };</code>

To retrieve the information stored in the object, you can use the following syntax:

<code>summon.name</code>

#### Dynamic typing

JavaScript is a "dynamically typed language", which means that, unlike some other languages, you don't need to specify what data type a variable will contain (numbers, strings, arrays, etc).

  - For example, if you declare a variable and give it a value enclosed in quotes, the browser treats the variable as a string. Even if the value enclosed in quotes is just digits, it is still a string — not a number — so be careful.

## Constants in JavaScript

As well as variables, you can declare constants. These are like variables except that:

 - you must initialize them when you declare them

 - you cannot assign them a new value after you have initialized it

Note that although a constant in JavaScript must always name the same value, you can change the content of the value that it names. This isn't a useful distinction for simple types like numbers or booleans, but consider an object:

<code>const junction = { guardianForce : 'Ramuh' };</code>

<code>console.log(junction.guardianForce); // 'Ramuh'</code>

You can update, add, or remove properties of an object declared using const, because even though the content of the object has changed, the constant is still pointing to the same object:

<code>junction.guardianForce = 'Doomtrain';</code>

<code>console.log(junction.guardianForce); // 'Doomtrain'</code>

#### When to use const and when to use let

If you can't do as much with <code>const</code> as you can with <code>let</code>, why would you prefer to use it rather than let? In fact const is very useful. If you use const to name a value, it tells anyone looking at your code that this name will never be assigned to a different value. Any time they see this name, they will know what it refers to.

In this course, we adopt the following principle about when to use let and when to use const:

  - Use <code>const</code> when you can, and use <code>let</code> when you have to.

**This means that if you can initialize a variable when you declare it, and don't need to reassign it later, make it a constant.**
