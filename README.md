# Regex-Learning
Week 17 project
# Regex expressions and Matching Numbers! 

Regex expressions or Regular Expressions are a useful way to articulate searching text for possibilities or articulate character placements. 

We can use regex expressions to do things like look for certain words in a documents to identifying social security number to telephone numbers. This can allow for a number of uses like scrubbing for these kinds of things or looking up specific words. Regex has a number of uses in the coding world 

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

## Table of Contents

- [Character Classes](#character-classes)
- [Alternators] (#alternators)
- [The OR Operator](#the-or-operator)
- [Character Escapes](#character-escapes)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Flags](#flags)


## Regex Components

### Character Classes
 [abc] a-b-c [-.] dash or dot( if it is inside the [] that changes it from literal and it means or for every character entered into it.
alternation = other ways of saying

### Bracket Expressions
These are a list of characters and or character classes enclosed in brackets which are used to match single characters in a list or range of characters in a list. 

Stuff that appears inside of two brackets [] are optional it doesn't mean it doesn't have to be there is means or between all of the characters in the bracket.

Example [abc  (] --> a, or b, or c or space or parenthesis

### Characters and Escapes

    Literal characters:

      Capital R followed by 
      Lowercase a
      Lowercase i
      Lowercase n 
      Lowercase b 
      Lowercase o
      Lowercase w
      
      \. = literal period
      \[ = literal bracket

    Metacharacters = Character that does not indicate a literal character but a more generalized pattern. 

      Examples:
      First Match : \d\d\d any digit 0-9
      Add dashes: \d\d\d-\d\d\d-\d\d\d\d


      Can enable regex in use regex .*
      . = any character
      * = 0 or more (wildcard)


      Single Character
        - \d -> 0-9
        - \w -> A-Za-z0-9. // \W = NOT those
        - \s -> any whitespace (tab, space) // \S = NOT those
        - . -> any character whatsoever


Quantifiers 

      * = 0 or  More
	+ = 1 or More
	? = o or 1
	{min,max} minimum characters and maximum characters
	{n} number
	? = optional.(whatever character called before the Question mark is optional)can be that character or not 	there at all.

	colou?rs? = c-o-l-o-u-optional-r-s-optional


## Position
	
	Position
	^= beginning(can be the beginning of a character or beginning of the line. The ^ just means beginning you 	can get more specific by adding quantifiers and regex like \d)
	$ = end(this follows along the lines of the ^ character)
	\b = word boundary (this tells us where the word or whatever we choose ends or starts.)


### Breaking down our expression 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

	


'/ and \' indicate the beginning and the end of the expression
^ ensures the match starts at the beginning of a string
'()' the parenthesis capture the group for the beginning of the email address 
  - ([a-z0-9_\.-]+) to include any of these characters followed by the @sign with no spaces
  - @ the literal @ sign after the first group of the mail address
  - ([\da-z\.-]+) the second group of characters after the @ sign, still all with no spaces, followed by a literal 	period. 
  -\. the literal period. 
  - + one or more is the quantifier for how many in this group
  - ([a-z\.]{2,6}) the third group after the literal period (the domain which is usually .edu, .com, .gov etc)
  - {2,6} ends with characters between 2 and 6 lowercase letters.
  - + one or more is the quantifier for how many in this group
  - $ position indicates that it must end at the end of a string.
  

##Other Breakdowns into specifics
^\w+$ = any line that has a single word
\b\w{4}\b = any 4 letter word
\b\w{4,6}\b = any 4-6 letter word
\d{3}-\d{3}-\d{4}= matching numbers and a dash for looking for phone numbers that have a dash specifically
  

## Author
Michael Garner
Junior Developer - Student 
https://github.com/FirefighterMichael94

Thanks to: 
The Coding Train: https://youtu.be/c9HbsUSWilw?si=gOlbBdW64ZrOX1aN
Anchors article https://www.rexegg.com/regex-anchors.html#anywhere
Metacharacter list https://techdocs.broadcom.com/us/en/symantec-security-software/endpoint-security-and-management/symantec-mail-security-for-microsoft-exchange-server/7-10/Content-Filtering/about-metacharacters-SMSID0E1WAI-d4944e13363.html
