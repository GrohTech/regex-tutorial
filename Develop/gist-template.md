# RegEx Tutorial

If you've ever seen "RegEx" in a project, you might be wondering what that even means. It stands for "Regular Expression", which is basically a curated search pattern used to match strings for the purposes of identifying strings in large bodies of data, to replace or update characters within a string, or to validate user input.

## Summary

Let's go over a RegEx to match an email. 

You might be asking why that would be necessary. One reason would be to validate a new user's email address before it gets added to the database. 

A second step in this process might be to send a validation email, but to do that, you want to make sure that email gets sent to a real email address.

**Here is the RegEx we'll be breaking down:**
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

**Thinking about a real email address, here are some questions you might ask yourself before building your RegEx:**

1. Will I need to include any special characters - if so, which ones?
2. Will letters be included - if so, will they be uppercase, lowercase, or both?
3. Will there be any literal characters or strings - meaning, is there any piece of this string that will be the same every single time?
4. Will there be numbers to account for - if so, are all numbers acceptable? 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)
- [Email example breakdown](#email-example-breakdown)


## Regex Components

### Anchors

As opposed to other pieces of a RegEx sequence that match characters, anchors match positions of text within a string.


* **Caret anchor**

The `^` matches the beginning of the text within a string. You might use this to check for one specific character at the beginning of a string.


* **Dollar anchor**

The `$` matches the end of the text within a string. You might use this to check for one specific character at the end of a string.


* **Caret and Dollar anchor combination**

Often, the caret and dollar anchors are used in combination - as it is in our email match example, which starts with a `^` and ends with a `$` - to check if a whole string matches a pattern.

In the below RegEx example, the goal is to match with a time in this format: `xx:xx`. You could search for strings of time that match an exact pattern. 

Specifically, you'd start by checking for any digit, followed by any digit, followed by a colon, followed by any digit, and ending with any digit.
```
/^\d\d:\d\d$/
```

### Quantifiers

Quantifiers check for the quantity of a string or a piece of a string.


* **Quantity**

The `{n}` quantity quantifier measures how many of a certain character are needed, or to measure the smallest or largest quantities of that character, as is shown in the at the end of the email example: `{2,6}`.

In the below RegEx example, you'll check strings of phone numbers for grouped digits. 

Specifically, you'll check for 3 digits, followed by a hyphen, followed by 3 digits, followed by a hyphen, followed by 4 digits.
```
/^(\d{3})-(\d{3})-(\d{4})$/
```

* **Shorthands**


A commonly-used quantifier is `+`, meaning "one or more":

Another commonly-used quantifier is `*`, meaning "zero or more":


### Character Classes


Character classes match any character from a certain set.

`\d` checks for all digits between 0 and 9.

`\s` checks for spaces.

### Grouping and Capturing

Breaking up a more complicated string into smaller pieces and creating multiple patterns to match to those pieces is called "grouping and capturing". In fact, those simpler patterns that tackle small pieces of strings are called "capturing groups".

Because an email string is made up of so many pieces, and has so many possible variations, grouping and capturing is a great way to deal with those pieces.

Returning to the "matching an email" example, let's see how we'd break down a real email address into pieces, in preparation for grouping and capturing:

**First, come up with a few examples of email addresses:**

email@email.com
Email336@school.edu
fox_Searcher-4901@govjob.gov

**Let's break up one email address into pieces:**

| Group 1 | | Group 2 | | Group 3 |
| :--: | :--: | :--: | :--: | :--: |
| (fox_Searcher-4901) | @ | (govjob) | . | (gov) |
| (all letters (a-z), all numbers (0-9), underscores, slashes, dots, hyphens match as many times as possible) | must be an @ symbol | (all digits (0-9), all letters (a-z), periods, hyphens, match as many times as possible) | must be a period | (all letters, periods, length must be between 2 and 6 characters) |
| ([a-z0-9_\.-]+) | @ | ([\da-z\.-]+) | \. | ([a-z\.]{2,6}) | 

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

### Email example breakdown

Let's return to the email example:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

**First, come up with a few examples of email addresses:**

email@email.com
Email336@school.edu
fox_Searcher-4901@govjob.gov

**Let's break up one email address into pieces:**

| 1 | 2 | 3 | 4 | 5 |
| :--: | :--: | :--: | :--: | :--: |
| fox_Searcher-4901 | @ | govjob | . | gov |
| all letters (a-z), all numbers (0-9), underscores, slashes, dots, hyphens, match as many times as possible | must be an @ symbol | all digits (0-9), all letters (a-z), periods, hyphens, match as many times as possible | must be a period | all letters, periods, length must be between 2 and 6 characters |
| ([a-z0-9_\.-]+) | @ | ([\da-z\.-]+) | \. | ([a-z\.]{2,6}) | 

**Here are some questions you might ask yourself before building your RegEx:**

1. Will I need to include any special characters - if so, which ones?
2. Will letters be included - if so, will they be uppercase, lowercase, or both?
3. Will there be any literal characters or strings?
4. Will there be numbers to account for - if so, are all numbers acceptable? 

## Author

Hi All! I'm Lauren! Right now, I'm powering through the University of Wisconsin - Extended Campus Full Stack Coding Bootcamp. 

Please don't hesitate to reach out!

- [GitHub](https://github.com/GrohTech)
