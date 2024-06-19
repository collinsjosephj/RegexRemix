# Title: Anything but Regular, a Discussion about Password Strengh Validation & Regex

I would like to welcome you to this tutorial on regex, a inherantly powerful tool utilized by developers worldwide for pattern matching and text manipulation. Regex (short for Regular Expressions) can seem intimidating at first, however, it is a essential tool once one becomes proficient in the world of web development/full stack coding applications. In this tutorial, we will discuss a regex pattern used for ensuring that passwords are both strong and secure, thus keeping user profiles and sensative information secure on the internet. 

## Summary

The password validation regex pattern that we will be exploring today is as follows: `^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$`
This pattern is used to validate passwords, and ensures that the password chosen has at least one lowercase letter, one uppercase letter, one digit, one special character (i.e !, @, #, $, $...), and is at least 8 characters long. Like any password created in today's world, one is more than likely to meet the requirements previously mentioned. By the end of this tutorial, you will gain a better understanding of each component of this particular regex and how it works to enforce requirements pertaining to user password strength. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
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

Anchors are used in Regular Expression Patterns to assert particular position within the string. In this regex we are discussing:

   - The anchor `^` denoted is for denoting the position at the start of the line;
   - The anchor `$` is used to signify the end of the line

Now, lets discuss what happens and how one can manipulate what comes between the beginning and end of this pattern in the sections to follow!

### Quantifiers

Quantifiers are used to specifiy how many instances of a character, group, or certain character class must be present in the user input. In our regex, `{8,}` means that any preceding pattern outlined before must appear 8 (or more) times, and to be put simply, the password must be 8 characters long AND meet case/character requirements. Here are a few ways that you can manipulate this particular quantifier:

  - `{8}` can be used if you would like the inputed password to be exactly 8 characters long;
  - `{8, n}` can be used if you would like the password to be between 8 characters long, and no more than any given integer, that integer represented by "n";

In summary, changing the quantifiers are a way to control the requirements for matching patterns, such as the length of a password or how many times a certain character should appear. 

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
