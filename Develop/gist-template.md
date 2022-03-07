# Title (replace with your title)

Regex tutorial by Tanner Shahan

## Summary

We'll be looking into the Regex Email expression: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ 
This verifies the format that email addresses need to be in. For example: firstmiddlelastname@gmail.com, 123@gmail.com, etc. Let's Dive In

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

^ - This part matches the first part of the string. This signals a position and not necesarrily a character.
$ - This is the end of the string, and like above just signals a position.

### Quantifiers
{2,6}

### OR Operator
This regex is using two quantifiers, = and {2,6}.

In this part of the expression: [a-z0-9_.-]+ and this part:  [\da-z.-]+
says that any charcter that matches the characters inside the bracket is to be expected to show up at least once.

[a-z.]{2,6} shows that 2-6 characters that matches those inside the brackets are expected. 

### Character Classes

/d - is used to match any characters that's a digit. The slash is used to show that's it's not the letter.
/s - is used to match a white space character

"." - this matches any character, that doesn't necessarily require a backslash.

### Flags

Flags are parameters that can be added to an expression to have it search differently. 

Some Examples:
/Hi/ m matches all 'Hello's

### Grouping and Capturing

To group and capture you use: () in a regex.

Whatever is in the parentheses is recieved as a single group, and considers all the information to be a single unit.

so in our example: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

the three groups that are there are :([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}).

and can also be shown as: group1@group2.group3.

### Bracket Expressions
The last part of the Regex is bracket expressions.

Here they are in our code: 
[a-z0-9_.-], [\da-z.-], and [a-z.]

so for example the [a-z0-9_.-] part represents any lowercase letters (from a-z), a digit between 0-9, or following a period.

### Greedy and Lazy Match

A Greedy and/or Lazy Match examples:

<[^<>]+>  matches a character shown `<` or `>` once or multiple times to be included in `<` and `>`. 

### Boundaries

Boundaries are places between the characters that are a *Word* or *Not-A-Word*

### Back-references
 Back referencing is referring to a match that is captured and svaed in memory.

Example: ([xyz])\1

the \1 matches the same text that was referenced by the first capturing group

### Look-ahead and Look-behind

Look-ahead and Look-behind are "start" and "end" anchors that match charcters and returns the result: 
MATCH OR NO MATCH.


## Author

This tutorial is created by Tanner Shahan and can be found at <a href="github.com/bvsswave">Github</a>

Gist Link: https://gist.github.com/bvsswave/cfe4f5afb490aa8ffe85e39a1480047e