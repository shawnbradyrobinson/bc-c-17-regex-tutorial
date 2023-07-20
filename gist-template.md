# Matching an Email Regex 

Wouldn't it be nice to search for emails and only emails, without needing to write out literals in mulitple command-F searches of "@gmail.com", "@aol.com", or "@outlook.com"? 

Well, you're in luck! With the use of regular expressions, we can accomplish just the search you need, with only one query! 
## Summary

Today we will be looking at an email matching regex. The syntax for the regex is: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Let's jump right in to the details! 

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
The anchors for this regex are the "^" character and the "$" character. "^" signifies that the characters that follow are expected at the beginning of the searched string. "$" signifies that the characters that precede are expected at the end of the searched string. 
### Quantifiers
Within this regex, we have the quantifiers {2, 6} -- this means that we are looking to find a number of results for this search a minimum of two times and a maximum of six times. What follows from this is that the characters that follow the "." in our email must be betweeen two through six in total length. 

Think about common top level domains. ".com", ".org", ".io", etc... A great majority, if not all, are six characters or less in length. Thus, these quantifiers will work perfectly for our purposes! 
### Grouping Constructs
There are three sections of grouping within this regex, but all are fairly straight forward to understand, once you get the hang of it. 

In our first section, the regex states: [a-z0-9_\.-]

This means that it is looking for results from all characters "a" through "z", all numbers 0 through 9, as well as underscores "_", backslashes "\", dots ".", and hyphens "-".

This component of our email is where users will undoubtedly have the most flexibility, so it is only natural that this part of our regex needs to be the open and welcoming to various search matches. 

In the next section, the regex states: [\da-z\.-]

"\d" is a metacharacter that represents a search for a digit 0-9. It is also searching for lowercase characters "a" through "z" again, as well as backlashes, dots, and hyphens again. 

The final section of the regex states: [a-z\.]

As mentioned previously, this component of the regex represents the top level domain search, and so it is more limited in scope. Nevertheless, it is searching for matches of all lowercase characters "a-z", backslashes, and dots. 
### Character Classes
The only meta characters used within this regex are \d and "+" to join the three sections of searches together 
### The OR Operator
There are no OR operators within this regex
### Flags
There are no flags within this regex
### Character Escapes
There are no character escapes within this regex 

## Conclusion
Hopefully you have found this to be a helpful tutorial to dip your toes into the wonderful world or regexes!!! 
## Author

Shawn Robinson is junior software developer working in the Kansas City area. For more inquiries, he can be reached at: 

https://www.linkedin.com/in/shawn-robinson-9aaa12170/

