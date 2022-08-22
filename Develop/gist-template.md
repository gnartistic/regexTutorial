# Regex Tutorial for URL matching
This tutorial was created to help others understand how to use a regex, as well as to demonstrate my own understanding of regular expressions.

A regular expression (Regex/Regexp), is a special text string for describing a search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string.

### Example

This is a regular expression used for URL matching.

```/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ ```
 


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
