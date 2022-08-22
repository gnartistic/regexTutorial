# Regex Tutorial for URL matching
This tutorial was created to help others understand how to use a regex, as well as to demonstrate my own understanding of regular expressions.

A regular expression (Regex/Regexp), is a special text string for describing a search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string.

### Example

This is a regular expression used for URL matching.

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ ```
 
#### Explanation
| Character | Definition |
|-----------|:------------:|
|```/```|Begins regex.|
|```^```|This is always at the begining of the string to position the anchors.|
|```(```|Groups together multiple "tokens" to create a capture group. This can be uaed to retrieve a substring or back reference.|
|```https```|This indicates a sub-expression string that should be matched.|
|```?```|This is a greedy quantifier. It denotes 0 or 1 occurence of the pervious character, for example, making `https`, `http`.|
|```\/\/```|This is an escaped character.|
|```)```|This ends the captured group.|
|```?```|Greedy quantifier indicating the entire previous section wrapped.|
|```(```|Begins captured group.|
|```[```|Begins bracket list.|
|```/d```|This is a metacharacter indicaiong one any one digit character, 0-9.|
|```a-z```|This indicates lowercase letter between a-z.|
|```\.```|Escape sequence denoting the character `.`|
|```-```|This indicates the character `-`.|
|```]```|Ends bracket list.|
|```+```|Because this is outside the greedy quantifier, it is denoting that the previous bracket list characters may occur one or more times.|
|```)```|Ends captured group.|
|```\.```|Escape sequence denotiong the character `.`|
|```(```|Begins capture group.|
|```[```|Begins bracket list.|
|```a-z```|Indicates lowercase letters between a-z.|
|```]```|Ends backet list|
|```2-6```|Occurence indicator denoting the previous bracket list characters may occur from 2-6 times.|
|```)```|Ends captured group.|
|```(```|Begins captured group.|
|```[```|Begins bracket list.|
|```/```|Escapes regex to match the character `/`.|
|```\w```|This is a character class indicationg any dingle word characters. Those are any characters including a-z, A-Z, 0-9, and _.|
|```.```|Escape sequence denoting the character `.`|
|```-```|This indicated the `-` character.|
|```]```|Ends bracket list.|
|```*```|Greedy quantifier indicating that the entire previous captured group may occur zero or more times.|
|```/```|Escapes regex to denote the `/` character.|
|```?```|Greedy quanitifier indicating previous character `/` may have 0 or 1 occurence.|
|```$```|Position anchoring that ends the string.|
|```/```|Ends regex.|



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
The anchors are always at the beginning of the string. For the example above, ```^``` is the symbol to represent the beginning of the expression.

Side note: 
The ```$``` represents the end of the expression.

### Quantifiers
 Quantifiers communicate to the regex engine that it must match the quanity of the character or the expression to it's left. There are 2 types of quantifiers: greedy, and lazy. 
 
Please refer to the [example](#example) at the beggining of the tutorial.

 Explained:
 ```*``` and ```*?``` matches 0 or more times.
 ```+``` and ```+?``` matches 1 or more times.
 ```?``` and ```??``` matches 0 or 1 times.
 ```{n}``` and ```{n}?``` matches exactly n times.
 ```{n,}``` and ```{n,}?``` matches at least n times.
```{n,m}``` and ```{n,m}?``` matches from n to m times.

Examples:
```https?``` will match 'https' or 'http' because of the ```?```.
```[\da-z\.-]+``` will match a single digit, a group of letters (a-z), a dot (```.```), or a hyphen (```-```).  

### OR Operator

### Character Classes
Character classes ensure that a given sequence of characters matches a larger set of characters.

Please refer to the [example](#example) at the beggining of the tutorial.

Explained:
```[a-z]``` will match lowercase alphabetic characters, a through z.
```\w``` will match a single word.
```\d``` will match a single character that is a number, 0-9.
```.``` will match any character

### Flags

### Grouping and Capturing
Grouping expressions allows us to keep things more organized and easier to exact the characters of any given group. To group expressions we use parenthesis ```()```.

Please refer to the [example](#example) at the beggining of the tutorial.

Explained:
```(https?:\/\/)``` this group means that the url can begin with either ```http://``` or ```https://```.
```([\da-z\.-]+)``` this group is the domain name. It matches 1 or more numbers, letters, dots, or hyphens.
```([a-z\.]{2,6})``` this group is connected with ```+```, this matches 2-6 copies of the sequences ```[a-z\.]```.


### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
