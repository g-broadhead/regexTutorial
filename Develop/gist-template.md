# Regex Tutorial 

This is a tutorial to explain Regex (regular expressions) are, how they work, and what they are used for.

## Summary

Regex is a string of text that allows you to create search patterns that match, manage, and locate text. 

This is an example of a regex to match E-mail addresses:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Regex can be used from the command line and in text-editors to find text within a file.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components
E-mail addresses:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

### Anchors
Anchors symbol ^ is a symbol used to signify a string that begins with the characters that follows it. The Anchor symbol $ is a symbol used to signify a string that ends with the characters before it. Regex is case-sensitive. Using ^Example, "Example" will match but "example" will not. 

For the email example, the pattern search starts with an ^ anchor and ends with an $ anchor. 

### Quantifiers
Quantifiers are used to set limits for the string. This includes a minimum and or maximum numbers or characters. By default, Quantifiers will match as many matches as possible. 
Limiting symbols are:
(*) — Matches the pattern zero or more times
(+) — Matches the pattern one or more times
(?) — Matches the pattern zero or one time
({}) — Curly brackets can provide three different ways to set limits for a match:
({ n }) — Matches the pattern exactly n number of times
({ n, }) — Matches the pattern at least n number of times
({ n, x }) — Matches the pattern from a minimum of n number of times to a maximum of x number of times

For the email example, some quantifiers are used. In the first and sencond group constructs, you can see the (+) quantifier is used to search for matches one or more times. In the final group, you can see the ({2,6}) being used to match the pattern for a minimum of 2 and maximum of 6.

### Grouping Constructs
Grouping Constructs are used to set characters into groups. This is used to check multiple parts of a string. To do this, you use parenthesis (()). Each section in parentehsis are known as subexpressions. 

For the email example, you can see the sections of an email are broken up into groups: "([a-z0-9_\.-]+)" @ "([\da-z\.-]+)" \. "([a-z\.]{2,6})"

### Bracket Expressions
Anything inside a set of square brackets ([]) represents a range of characters that we want to match. These symbols outline the characters we want to include in the search. A hyphen (-) is used between alphanumeric characters to show the desired range of possible characters. Examples: [a-g], [h-p], [q-z], [0-5], [6-9] 

If a string contains special characters, you can also include those sumbols in your bracket expressions. Examples: [_], [-], [#], [_-#]

For the email example, you can see bracket expressions used.
[a-z0-9_\.-] searches for A through Z, numbers 0 through 9 and special characters, ([\da-z\.-]+) searches for A through Z, ([a-z\.]{2,6}) searches for A through Z.

### Character Classes
Character Classes define sets of characters which can occur in an input string to match. 
Examples of character classes are:
(.) — Matches any character except the newline character (\n)
(\d) — Matches any Arabic numeral digit.
(\w) — Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). 
(\s) — Matches a single whitespace character, including tabs and line breaks.

For the email example, you can see (\d) is used to match any Arabic numeral digit 

### The OR Operator
OR Operator (|), is used to search for sets of alphanumeric characters in any order. For example: the expression [abc] could be written as (a|b|c). Using subexpressions, (a|b|c):(x|y|z), will match with "abc:xyz" and "acb:xyz" but not "xyz:abc".

### Flags
Flags are used to create exceptions to the literal characters. Flags are placed at the end of the regex and define any additional functionality or limits. 
Symbols used for flags are:
(g) — Global search
(i) — Case-insensitive search
(m) — Multi-line search

### Character Escapes
Character Escapes (\) are used in a regex to escape a character that would normally be interpreted literally. 

For the email example, the (\) negates the literal interpretation of the special character symbols. This will begate any special meaning these characters may have outside of the given representation. 

## Author

My name is Garrett and I am a Full-Stack Web Developer in training.
https://github.com/g-broadhead
