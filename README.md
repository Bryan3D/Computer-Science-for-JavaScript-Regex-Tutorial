

# <span style = "color:Yellow; font-weight:bold">Introduction to Regular Expressions in JavaScript:</span>

**`Regular Expressions`** in **`JavaScript`** are a sequence of characters used to match or search for patterns in text. Regex can be used to efficiently search and manipulate text in JavaScript. 

**`Use cases:`** Regex is widely used in text editors, search engines, and programming languages, including JavaScript.


# <span style = "color:yellow; font-weight:bold">Summary</span>
JavaScript Regular Expressions **`(RegEx)`** are a sequence of characters used to match or search for patterns in text. They can be created using either literal notation (enclosing the pattern in forward slashes) or using the RegExp object constructor. RegEx has special characters called metacharacters that have specific meaning, such as the dot (.) to match any character except newline, the asterisk (*) to match zero or more occurrences of preceding character, the plus (+) to match one or more occurrences of preceding character, the question mark (?) to match zero or one occurrence of preceding character, and character sets ([abc]) to match any one of the characters in the set. RegEx can be tested in JavaScript using the test() method, which returns a Boolean value indicating whether the pattern matches the string, and the exec() method, which returns an array containing the match and capturing groups.

##  <span style = "color:Red; font-weight:bold">Table of Contents</span>

- [Introduction to Regular Expressions in JavaScript:](#introduction-to-regular-expressions-in-javascript)
- [Summary](#summary)
  - [Table of Contents](#table-of-contents)
- [Creating Regular Expressions in JavaScript:](#creating-regular-expressions-in-javascript)
  - [`Literal Notation:`](#literal-notation)
  - [`Constructor Notation:`](#constructor-notation)
- [ Basic Regex Syntax and Special Characters:](#-basic-regex-syntax-and-special-characters)
  - [`Literals`](#literals)
  - [`.(dot)`](#dot)
  - [`+(plus)`](#plus)
  - [`?(question mark)`](#question-mark)
  - [`\(backslash)`](#backslash)
  - [`Character sets`](#character-sets)
  - [`Anchors`](#anchors)
  - [`Quantifiers`](#quantifiers)
  - [`Grouping Constructs`](#grouping-constructs)
  - [`Bracket expressions`](#bracket-expressions)
- [Testing Regular Examples:](#testing-regular-examples)
  - [JavaScript](#javascript)
  - [SQL](#sql)
- [Author](#author)
- [MIT License](#mit-license)




# <span style = "color:Yellow; font-weight:bold">Creating Regular Expressions in JavaScript:</span>

## `Literal Notation:`

A regular expression can be created using the literal notation by enclosing the pattern in forward slashes ( / ). 

For example:

`var pattern = /Hello/;`


## `Constructor Notation:` 

A regular expression can also be created using the RegExp object constructor. 

For example:

`var pattern = new RegExp("Hello");`




# <span style = "color:Yellow; font-weight:bold"> Basic Regex Syntax and Special Characters:</span>

## `Literals` 

Any character in the regex pattern will match the same character in the text.
Metacharacters: Special characters used to match a pattern in text, 

for example:

## `.(dot)` 

matches any character except newline
(asterisk) matches zero or more occurrences of preceding character.

## `+(plus)` 

matches one or more occurrences of preceding character.

## `?(question mark)` 

matches zero or one occurrence of preceding character

## `\(backslash)` 

used to escape a special character and treat it as a literal

## `Character sets`

Used to match any one of the characters in the set. 

for example:

`[abc]` matches any character a, b, or c


`[^abc]` matches any character except a, b, or c

## `Anchors`
anchors are special characters that match a position rather than a character. There are two types of anchors in RegEx:

Start of Line (^): Matches the position at the start of a line.

End of Line ($): Matches the position at the end of a line.

These anchors are used to specify the beginning or end of a line as the starting or ending point of the pattern to be matched. For example, the pattern "^A" matches any line that starts with the letter "A", while the pattern "end$" matches any line that ends with the word "end".

## `Quantifiers`

in regular expressions are used to specify the number of times a pattern should match. There are several quantifiers in RegEx:

(asterisk): Matches zero or more occurrences of the preceding pattern. 

For example, 

the pattern `"a*"` matches zero or more occurrences of the letter `"a"`.
(plus sign): Matches one or more occurrences of the preceding pattern. For example, the pattern `"a+"` matches one or more occurrences of the letter `"a"`.
`? (question mark):` Matches zero or one occurrence of the preceding pattern. For example, the pattern "a?" matches zero or one occurrence of the letter `"a"`.

`{n}(curly braces)`: Matches exactly "n" occurrences of the preceding pattern. 

For example

the pattern `"a{3}"` matches exactly three occurrences of the letter `"a"`.

`{n,} (curly braces with comma)`: Matches at least `"n"` occurrences of the preceding pattern. For example, the pattern `"a{2,}"` matches two or more occurrences of the letter `"a"`.

`{n,m} (curly braces with comma and another number)`: Matches at least "n" and at most `"m"` occurrences of the preceding pattern. For example, the pattern `"a{1,3}"` matches one, two or three occurrences of the letter `"a"`.

These quantifiers allow you to specify the exact number of times a pattern should match, or to match a pattern any number of times, from zero to many.

## `Grouping Constructs`

Are used to define subexpressions within a larger pattern. These subexpressions can be treated as a single unit, allowing for more complex and flexible matching and manipulation of text. Grouping constructs in regular expressions are denoted by parentheses ( ), and the contents of a group can be referred to by backreferencing. For example, a group can be used to match a repeating pattern, or to extract a specific portion of the matched text for further processing. Grouping constructs are widely used in many programming languages that support regular expressions.

## `Bracket expressions`

are a type of grouping construct in regular expressions that allow for the creation of character sets. A bracket expression is denoted by square brackets `[ ]` and can contain a range of characters, including letters, numbers, and special characters. The expression matches any single character that is contained within the brackets. For example, the expression `[0123456789]` matches any digit, and the expression `[a-zA-Z]` matches any letter. Bracket expressions can also contain special characters such as `^` and `-` that have special meanings in the context of character sets. For example, the expression `[^0-9]` matches any character that is not a digit. Bracket expressions provide a convenient way to specify a set of characters that can match a particular pattern in the text.






# <span style = "color:Yellow; font-weight:bold">Testing Regular Examples:<span>

`The test() method can be used to test if a pattern matches a string.`


For example:

## JavaScript

var pattern = /Hello/;

console.log(pattern.test("Hello World"));

// returns true

console.log(pattern.test("Goodbye World"));

// returns false


<b>*`The exec() method can be used to find and return a match, as well as capturing groups.`*


## SQL

`var pattern = /Hello (\w+)/;`

`var result = pattern.exec("Hello World");`

console.log(result[0]);

// returns `"Hello World"`

console.log(result[1]);

// returns `"World"`


# <span style = "color:Yellow; font-weight:bold">Author</span>

This tutotial is created for Bryan A Quero
Feel free to contact me at bryanq2008@live.com with any questions about this tutorial. Visit https://github.com/Bryan3D to see more of my projects.

# <span style = "color:Yellow; font-weight:bold">MIT License</span>
Copyright (c) [2023] [`Introduction to Regular Expressions in JavaScript`]

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.