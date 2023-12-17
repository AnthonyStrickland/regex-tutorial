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

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
