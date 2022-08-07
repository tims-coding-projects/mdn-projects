# Useful string methods

## Finding the length of a string

- variable.length

## Retrieving a specific string character

- variable[0]

## Testing if a string becomes a substring {includes()}

- if (browserType.includes('zilla')) {
  console.log('Found zilla!');
} else {
  console.log('No zilla here!');
}

## Testing if starts or ends with substring {startsWith(); endsWith()}

- const browserType = 'mozilla';

if (browserType.startsWith('zilla')) {
  console.log('Found zilla!');
} else {
  console.log('No zilla here!');
}


- const browserType = 'mozilla';

if (browserType.endsWith('zilla')) {
  console.log('Found zilla!');
} else {
  console.log('No zilla here!');
}

## Finding a position of a substring in a string {indexOf()}

- const tagline = 'MDN - Resources for developers, by developers';
  console.log(tagline.indexOf('developers')); // 20

- will return -1 if character is not in the string

- to find subsequent occurrences of a string

- const firstOccurrence = tagline.indexOf('developers');
  const secondOccurrence = tagline.indexOf('developers', firstOccurrence + 1);

  console.log(firstOccurrence); // 20
  console.log(secondOccurrence); // 35
  
## Extracting a substring from a string {slice()}

- const browserType = 'mozilla';
  console.log(browserType.slice(1, 4)); // "ozi"
  
- If you know that you want to extract all of the remaining characters in a string after a certain
  character you do not have to include the second parameter.
  
   - browserType.slice(2); // "zilla"
   
## Changing case {toLowerCase(), toUpperCase()}

- const radData = 'My NaMe Is MuD';
  console.log(radData.toLowerCase()); // my name is mud
  console.log(radData.toUpperCase()); // MY NAME IS MUD
  
## Updating parts of a string {replace()}

- In this example, we're providing two parameters — the string we want to replace and the string we
  want to replace it with:
  
  - const browserType = 'mozilla';
    const updated = browserType.replace('moz','van');

    console.log(updated);      // "vanilla"
    console.log(browserType);  // "mozilla"

- Note that replace(), like many string methods does not change the string it was called on, but
  returns a new string. If you want to update the original browserType variable you would have to
  do something like this:
  
  - let browserType = 'mozilla';
    browserType = browserType.replace('moz','van');

    console.log(browserType);  // "vanilla"

- Also note that we now have to declare browserType using let, not const, because we are reassigning 
  it.
  
- Be aware that replace() in this form only changes the first occurrence of the substring. If you want
  to change all occurences use replaceALL():
  
  - let quote = 'To be or not to be';
    quote = quote.replaceAll('be','code');

    console.log(quote);  // "To code or not to code"




