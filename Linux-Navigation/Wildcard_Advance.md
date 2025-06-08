# Wildcards

Wildcards allow you to select filenames based on patterns of characters. The table below lists the wildcards and what they select:

## Summary of wildcards and their meanings

|Wildcard|Meaning|
|:---|:---|
|*|Matches any characters|
|?||Matches any single character|
|[characters]|Matches any character that is a member of the set characters. The set of characters may also be expressed as a POSIX character class such as one of the following:

POSIX Character Classes

|[:alnum:]|Alphanumeric characters|
|[:alpha:]|Alphabetic characters|
|[:digit:]|Numerals|
|[:upper:]|Uppercase alphabetic characters|
|[:lower:]|Lowercase alphabetic characters|
|[!characters]|Matches any character that is not a member of the set characters|

Using wildcards, it is possible to construct very sophisticated selection criteria for filenames. Here are some examples of patterns and what they match:


Examples of wildcard matching
Pattern	Matches
*	
All filenames

g*	
All filenames that begin with the character "g"

b*.txt	
All filenames that begin with the character "b" and end with the characters ".txt"

Data???	
Any filename that begins with the characters "Data" followed by exactly 3 more characters

[abc]*	
Any filename that begins with "a" or "b" or "c" followed by any other characters

[[:upper:]]*	
Any filename that begins with an uppercase letter. This is an example of a character class.

BACKUP.[[:digit:]][[:digit:]]	
Another example of character classes. This pattern matches any filename that begins with the characters "BACKUP." followed by exactly two numerals.

*[![:lower:]]	
Any filename that does not end with a lowercase letter.
