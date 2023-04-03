# Regex Matching a URL

A regular expressions is a pattern that is used to match character combinations in strings. This allows for a wide variety of uses, such as: verifying emails, setting passwords validators and checking for URL's as well as many more.

## Summary

In this how-to, we will parse the expression and analyse the components used to match URLs.
A URL (Uniform Resource Locator) is a reference to a web resource that specifies its location on a computer network and a process of retrieving it. The regular expression we will be looking at is: /^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/

## Table of Contents

- [Anchors](#anchors)

- [Quantifiers](#quantifiers)

- [Character Classes](#character-classes)

- [Grouping and Capturing](#grouping-and-capturing)

- [Regex Components](#regex-components)

Regex Components

### Anchors

/^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/
Anchors are used to define the position where the regex pattern should match in the string. The caret (^) matches the position before the first character in the string, while the dollar sign ($) matches the position right after the last character in the string.

### Quantifiers

/^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. The quantifiers used for this regex are: ?, +, _, and {2,6}. The ? indicates 0 or 1 occurrence, + indicates one or more occurrences, _ indicates 0 or more occurrences, and {2,6} specifies a range, meaning between 2 and 6 occurrences.

### Character Classes

/^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/
Character classes are used to define the type of characters to expect. In our example, we have [\da-z.-], [a-z.], and [/\w .-]. Here, \d matches any digit, a-z matches any lowercase letter, . matches the literal dot character, \w matches any word character (letters, digits, or underscores), and / matches the literal forward slash character.

### Grouping and Capturing

/^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/
Grouping and capturing are used to apply quantifiers to a sequence of characters or to store the matched content for later use. In our regex, we have four capturing groups: (https?://), ([\da-z.-]+), ([a-z.]{2,6}), and ([/\w .-]\*). The first group matches the http or https, the second group matches the domain name, the third group matches the top-level domain (TLD), and the fourth group matches the path.

### Regex Components

/^(https?://)?([\da-z.-]+).([a-z.]{2,6})([/\w .-])/?$/
Now, let's break down the regex:
^: Asserts the position at the start of the string.
(https?://)?: Matches the optional http or https protocol, followed by the literal '://' characters.
([\da-z.-]+): Matches one or more domain name characters (letters, digits, dots, or hyphens).
.: Matches the literal dot character.
([a-z.]{2,6}): Matches 2 to 6 TLD characters (letters or dots).
([/\w .-]*): Matches 0 or more path characters (forward slashes, word characters, spaces, dots, or hyphens).
: Indicates that the previous group ([/\w .-]) can be repeated 0 or more times.
/: Matches the optional literal forward slash character at the end of the URL.
$: Asserts the position at the end of the string.

OR Operators, Flags, Greedy and Lazy Match, Boundaries, Back-references and Look-ahead and Look-behind are not used for a URL Regex.

## Author

Hello, I am JJ. I am a student at LPS UPENN Fullstack Web-Developer Bootcamp. Check out my GitHub [JeevanMKJ](https://github.com/JeevanMKJ) it does not have much yet, but soon you will not want to look an anything else do to the magnetism of my incredibly DRY and sophisticated code.
