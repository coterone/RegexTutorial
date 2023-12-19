# Regex Tutorial - Data Validation
Regex, short for regular expressions, is a powerful and flexible sequence of characters that defines a search pattern. It is a tool used for pattern matching within strings. Regular expressions are widely used in programming, text processing, and data validation tasks. They provide a concise and efficient way to search, match, and manipulate text based on specific patterns.

## Summary

Use regex to validate user input, such as email addresses, phone numbers, zip codes, or credit card numbers. For example, ensuring that an email address follows the pattern user@example.com.

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

Anchors, such as ^ and $, act as precision tools. ^ asserts the beginning of a line, ensuring the pattern starts there. $ asserts the end, guaranteeing the pattern spans the entire input. This ensures exact positioning in the text.

(./assets/anchors.png)

The text string containing the words "start" and "end." The ^ in /^start/ asserts that "start" must occur at the beginning of the string, and the /end$/ asserts that "end" must occur at the end of the string. Both assertions return true because the text conforms to these patterns.


### Quantifiers
Think of quantifiers as control mechanisms for repetition. *, +, and ? manage varying degrees of occurrence, while {n}, {n,}, and {n,m} provide fine-tuned control over specific numerical requirements, offering a meticulous approach to pattern repetition.

(./assets/quantifiers.png)

The pattern /ab*/g is used to match sequences of "a" followed by zero or more "b" characters. The g flag ensures a global search, finding all matches in the text. As a result, the output is an array with the matched sequences.

### Grouping Constructs
Parentheses not only provide structure but act as organizers. They create logical units within the pattern, allowing you to apply quantifiers or modifiers to specific sections. This facilitates both clarity in pattern design and precision in extraction.

(./assets/groupingContructs.png)

This snippet uses grouping with (\w+) to capture words in the text. The overall pattern (\w+) (\w+) (\w+) captures three sets of words separated by spaces. The match function returns an array, and resultGroups.slice(1) extracts the captured groups, resulting in an array of the captured words.

### Bracket Expressions
Square brackets introduce a curated selection of characters. They form a character class, where any character within the brackets is a valid match. This selective approach enhances pattern specificity and avoids unnecessary matches

(./assets/bracketExpressions.png)

Here, [0-9]+ represents one or more digits, and \w+ represents one or more word characters. The pattern [0-9]+ \w+ matches sequences of digits followed by a space and then word characters. The output is an array containing the matched sequences.

### Character Classes
Character classes, denoted by \d, \w, and \s, represent predefined sets of characters. These shortcuts are like linguistic modules, enhancing the expressiveness of patterns by encapsulating common character types.

(./assets/characterClasses.png)

The pattern \w\d matches a word character followed by a digit. The match function returns an array containing all the matched sequences in the text.

### The OR Operator
The | symbol introduces an element of choice within the pattern. It's akin to a logical switch, allowing for alternatives. This versatility is especially powerful when dealing with variations in data formats or preferences.

(./assets/ORoperators.png)

The pattern /cat|dog/g uses the | symbol as the OR operator, matching either "cat" or "dog." The output is an array containing both matched words.

### Flags
Flags, such as (?i) and (?m), introduce meta-rules. They modify the behavior of the entire pattern. For instance, enabling case insensitivity or multiline mode extends the adaptability of regex to diverse scenarios.

(./assets/flags.png)

The /world$/m pattern uses the m flag to enable multiline mode. It asserts that "world" must occur at the end of a line. The test function returns true because the pattern matches the end of the second line in the text.

### Character Escapes
The backslash \ serves as a contextual key. It transforms special characters from operators to literals. This escape mechanism ensures that characters like . or \\ are treated as themselves, avoiding unintended interpretations.

(./assets/characterClasses.png)

The pattern /\./ uses the backslash \ to escape the dot . character. It matches a literal dot in the text, and the test function returns true because the pattern is found in the input.

## Author
This tutorial was created by a Full Stack web development bootcamp student.

Github: https://github.com/coterone

