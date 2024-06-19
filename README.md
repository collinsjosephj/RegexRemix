# Title: Anything but Regular, a Discussion about Password Strengh Validation & Regex

I would like to welcome you to this tutorial on regex, a inherantly powerful tool utilized by developers worldwide for pattern matching and text manipulation. Regex (short for Regular Expressions) can seem intimidating at first, however, it is a essential tool once one becomes proficient in the world of web development/full stack coding applications. In this tutorial, we will discuss a regex pattern used for ensuring that passwords are both strong and secure, thus keeping user profiles and sensative information secure on the internet. 

## Summary

The password validation regex pattern that we will be exploring today is as follows: `^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$`
This pattern is used to validate passwords, and ensures that the password chosen has at least one lowercase letter, one uppercase letter, one digit, one special character (i.e !, @, #, $, $...), and is at least 8 characters long. Like any password created in today's world, one is more than likely to meet the requirements previously mentioned. By the end of this tutorial, you will gain a better understanding of each component of this particular regex and how it works to enforce requirements pertaining to user password strength. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
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

As you may have picked up previously, character classes are used to match a set of characters. In our regex for example, `[a-z]` is used to match any lowercase letter inputed, `[A-Z]` is used for matching any uppercase letter, `/d` is used for any digit, and lastly, `[@$!%*?&]` matches any of the specified special characters. 

### Grouping and Capturing

Grouping and capturing are used to group certain parts of the regex pattern together, just as one would see prefixes and/or suffixes in linguistics. In our regex, the parantheses `()` are used for grouping. 

  - `(?=.*[a-z])`: ensures that there is at least 1 lowercase letter in the string (from "a" to "z"), and that it doesnt matter where in particular it appears, but it has to be there. 
  - `(?=.*[A-Z])`: ensures that there is at least 1 uppercase letter in the string (from "A" to "Z"), and that it doesnt matter where in particular it appears, but it has to be there. 
  - `(?=.*\d)`   : ensures that there is at least 1 number, in the string (from "0" to "9"), and that it doesnt matter where in particular it appears, but it has to be there. 
  - `(?=.*[@$!%*?&])`: ensures that a special character must be used somewhere in the string. 

### Look-ahead Assertions

Look-ahead assertions are a way to ensure that a certain pattern can be matched ahead in the string, without consuming characters. What does that mean?  Lets take an example from our previous section, `(?=.*[a-z])`, where the `?=` is a positive look-ahead, and checks that something is true ahead in the string, without actually moving the pointer in the string. Simply put, it makes sure that whatever is held within the `()`, in this case, the requirements for a lowercase letter, denoted by `[a-z]` can be found later in the string. For example, if an inputed password was as follows, `PASSWORD123!`, our look-ahead `(?=.*[a-z])` would determine that there is no lowercase letter included, so that password would not match the requirements. Similary, there are "look-behinds" assertions, which analyze whether or not the subpattern happens before the the asserting position (grouping), however, in this case, it is not utilized. 

### Wrapping it Up

Now that we have discussed this regex pattern for password validation, I hope that you have gained a basic understanding and just how powerful, if done right, this seemingly random assortment of characters you find on your keyboard can be! It is easier to understand once you divide and conquer, breaking down each part individually. This is not a one-size-fits-all expression, but being able to take this discussion and use it to better understand whatever regex pattern you might use for your own application is exactly where the fun begins! Best of luck, and thank you for joining me today. 

## Author


