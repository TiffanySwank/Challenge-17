# Challenge-17

## Tiffany Swank

### User Story

AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines

### Acceptance Criteria

GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile


# Example Regex 
^https?://(www\.)?example\.com$

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

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

^: This is the caret symbol (^), and it represents the start of the line or start of the string anchor. It specifies that the regex pattern must match from the beginning of the line or string.

$: This is the dollar symbol ($), and it represents the end of the line or end of the string anchor. It specifies that the regex pattern must match up to the end of the line or string.

### Quantifiers

Quantifiers specify the quantity of characters or expressions to match to the left.

* and *?: Match zero or more times.
+ and +?: Match one or more times.
? and ??: Match zero or one time.
{n} and {n}?: Match exactly n times.
{n,} and {n,}?: Match at least n times.
{n,m} and {n,m}?: Match from n to m times.

### Character Classes

[a-z]: Matches lowercase alphabetic characters from 'a' to 'z'.
\w: Matches a single word character.
\d: Matches a single digit (0-9).
.: Matches any character.

### Flags

### Grouping and Capturing

Grouping expressions use parentheses () to organize and capture characters.

(https?:\/\/): Matches URLs beginning with "http://", "https://", or none.
([\da-z\.-]+): Captures domain names, matching 1 or more numbers, letters, dots, or hyphens.
([a-z\.]{2,6}): Matches 2-6 copies of the sequence "[a-z.]".
([\/\w \.-]*): Matches multiple directories or path segments with "*" allowing any number of occurrences.

### Bracket Expressions

Bracket expressions are defined within "[]" brackets. Here are examples from our tutorial:

[\da-z\.-]: Matches a single character that is a digit, lowercase letter, dot, or hyphen.
[a-z\.]: Matches a single lowercase alphabetic character or a dot.
[\/\w \.-]: Matches a single character that is a forward slash, word character, space, dot, or hyphen.

### Greedy and Lazy Match

Greedy and lazy matching refer to how a regex quantifier (*, +, ?, {}) behaves when it comes to matching multiple occurrences of a character or group. Greedy matching attempts to match as many characters as possible, while lazy (or non-greedy) matching attempts to match as few characters as possible.

Greedy: \d+ matches the entire string "12345" because it greedily matches as many digits as possible.
Lazy: \d+? matches the first digit "1" because it lazily matches as few digits as possible.

### Boundaries

In regex, boundaries are used to specify positions within the text where matches should occur. Common boundary assertions include:

^: Asserts the start of a line or string.
$: Asserts the end of a line or string.
\b: Asserts a word boundary (where a word character transitions to a non-word character and vice versa).
\B: Asserts a non-word boundary.

^regex: Matches when the string starts with "regex."
regex$: Matches when the string ends with "regex."
\bword\b: Matches the word "word" as a whole word within the text.
\Bword\B: Matches "word" only when it's part of a longer word, not as a standalone word.

### Back-references
Back-references allow you to refer to and match the same text that was previously captured by a capturing group in the regex pattern. They are often used to find repeated occurrences of the same text.

Regex: (\b\w+\b) \1
String: "hello hello world world"
This regex uses a capturing group (\b\w+\b) to capture a whole word and then uses \1 to refer back to the first captured word. It will match "hello hello" and "world world" in the string.

### Look-ahead and Look-behind

Look-ahead and look-behind assertions are used to check for the presence (or absence) of certain patterns ahead or behind the current position in the text without consuming characters.
Regex: apple(?= pie)
String: "I love apple pie"
In this regex, (?= pie) is a positive look-ahead. It checks if "apple" is immediately followed by " pie" (with a space). It matches "apple" in the string because it satisfies the look-ahead condition.

## Author
Tiffany Swank
