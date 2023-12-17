# Street Address - Regex Tutorial

As a web development student I will explain the different part of a Regular Expression or regex so that I can better understand the search pattern the regex defines

## Summary

Regex are patterns used to match character combinations in strings. This tutorial is going to explain the use of regex to match street addreses using the expression  ^\\d+\\s[A-z]+\\s[A-z]+(\\s[A-z]+)?,\\s[A-z]{2}\\s\\d{5}(-\\d{4})?$ .  This can be useful when searching long documents that have multiple address you either need to find or omit.

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

### Anchors
Anchors provide a way to limit how a regex matches a particular string by telling the regex engine where matches can begin and where they can end.

^: Anchor matches the beginning of the text.  
$: Anchor matches the end of the text.       

### Quantifiers

Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. Some quantifiers have two versions, a greedy quantifier which tries to match an emlement as many times as possible.  A lazy quantifier which tries to match an element as few times as possible.  You can turn a greedy quantifier into a lazy quantifier just by addint a ? at the end.

+: Matches one or more times it is used after //d to match one or more digits
{5}: Matches exactly 5 times also used after //d to match 5 digits
?: Matches 0 or one time, it is used after the capturing group (-\\d{4}) to make it optional.

### Grouping Constructs

Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following: Match a subexpression that's repeated in the input string.

(\\s[A-z]+)?: This is a capturing group that matches an optional space followed by one or more letters. The captured text can be referred to later, either within the regex itself or in the surrounding code.
(-\\d{4})?: This is a capturing group that matches an optional hyphen followed by exactly four digits. The captured text can be referred to later, either within the regex itself or in the surrounding code.

### Bracket Expressions

A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions.

[A-z]: Matches any character in the range of characters separated by the -.

### Character Classes

A character class is a set of characters enclosed within square brackets. It specifies the characters that will successfully match a single character from a given input string.

[A-z]: This is a character class that matches any uppercase or lowercase letter.

### The OR Operator

Alternation is the term in regular expression that is actually a simple “OR”. In a regular expression it is denoted with a vertical line character | . Since looking for an address is specific there is no OR operator used.  If I wanted to find a street, blvd, ave, pkwy. the corresponding regexp: street|blvd|ave|pkwy.

### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching. A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.  Since the regex used does not use any flags, common flags are:

i: Case-insensitive matching.
g: Global matching.
m: Multiline mode

### Character Escapes

Regex recognizes common escape sequences such as \n for newline, \t for tab, \r for carriage-return, \nnn for a up to 3-digit octal number, \xhh for a two-digit hex code, \uhhhh for a 4-digit Unicode, \uhhhhhhhh for a 8-digit Unicode.

## Author

You can view more of my projects at https://github.com/AnthonyStrickland?tab=repositories

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
