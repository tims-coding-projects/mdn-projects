# Useful string methods

---

- Source: https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods

#### Strings as objects

Most things are objects in JavaScript. When you create a string, for example by using

<code>const string = 'This is my string';</code>

your variable becomes a string object instance, and as a result has a large number of properties and methods available to it. You can see this if you go to the String object page and look down the list on the side of the page!

Now, before your brain starts melting, don't worry! You really don't need to know about most of these early on in your learning journey. But there are a few that you'll potentially use quite often that we'll look at here.

#### Finding the length of a String

This is easy — you use the length property. Try entering the following lines:

<code>const browserType = 'mozilla';</code>

<code>browserType.length; // Returns 7</code>

This should return the number 7, because "mozilla" is 7 characters long. This is useful for many reasons; for example, you might want to find the lengths of a series of names so you can display them in order of length, or let a user know that a username they have entered into a form field is too long if it is over a certain length.

#### Retrieving a specific string character

On a related note, you can return any character inside a string by using square bracket notation — this means you include square brackets ([]) on the end of your variable name. Inside the square brackets you include the number of the character you want to return, so for example to retrieve the first letter you'd do this:

<code>browserType[0]; // Returns 'm'</code>

To retrieve the last character of any string, we could use the following line, combining this technique with the length property we looked at above:

<code>browserType[browserType.length-1]; // Returns 'a'</code>

The length of the string "mozilla" is 7, but because the count starts at 0, the last character's position is 6; using length-1 gets us the last character.

#### Testing if a string contains a substring

Sometimes you'll want to find if a smaller string is present inside a larger one (we generally say if a substring is present inside a string). This can be done using the includes() method, which takes a single parameter — the substring you want to search for.

It returns true if the string contains the substring, and false otherwise.

Often you'll want to know if a string starts or ends with a particular substring. This is a common enough need that there are two special methods for this: startsWith() and endsWith()

#### Finding the position of a substring in a String

You can find the position of a substring inside a larger string using the indexOf() method. This method takes two parameters – the substring that you want to search for, and an optional parameter that specifies the starting point of the search.

If the string contains the substring, indexOf() returns the index of the first occurrence of the substring. If the string does not contain the substring, indexOf() returns -1.
