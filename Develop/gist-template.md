# RegEx Tutorial

If you've ever seen "RegEx" in a project, you might be wondering what that even means. It stands for "Regular Expression", which is basically a curated search pattern used to match strings for a particular reason.

## Summary

Let's go over a RegEx to match an email. 

You might be asking why that would be necessary. One reason would be to validate a new user's email address before it gets added to the database. 

A second step in this process might be to send a validation email, but to do that, you want to make sure that email gets sent to a real email address, which brings us back to creating a RegEx to match an email.

Here is the RegEx we'll be breaking down:
```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

First, come up with a few examples of email addresses:

email@email.com
Email336@school.edu
fox_Searcher-4901@govjob.gov

Here are some questions you might ask yourself before building your RegEx:

1. Will I need to include any special characters - if so, which ones?
2. Will letters be included - if so, will they be uppercase, lowercase, or both?
3. Will there be any literal characters or strings?
4. Will there be numbers to account for - if so, are all numbers acceptable? 



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

### Quantifiers

Pro-tip:
Add the below RegEx to match before or after something specific to match ANYTHING else. 
.*
For example, if you wanted to search for 

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Hi All! I'm Lauren! Right now, I'm powering through the University of Wisconsin - Extended Campus Full Stack Coding Bootcamp. 

Please don't hesitate to reach out!

- [GitHub](https://github.com/GrohTech)
