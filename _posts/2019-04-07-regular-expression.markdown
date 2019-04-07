## Introduction
This blog is from [https://www.youtube.com/watch?v=sa-TUpSx1JA](https://www.youtube.com/watch?v=sa-TUpSx1JA)

Below are some rules and examples for regular expression.

## 常规表达式

| expression | meanings |
| :--------- | :---------------------- |
| .    | Any Character Except New Line |
| \d   | Digit (0-9)
| \D   | Not a Digit (0-9) |
| \w   | Word Character (a-z, A-Z, 0-9, -) |
| \W   | Not a Word Character |
| \s   | Whitespace (space, tab, newline) |
| \S   | Not Whitespace (space, tab, newline) |
| \b   | Word Boundary |
| \B   | Not a Word Boundary |
| ^    | Beginning of a String |
| $    | End of a String |
| []   | Matches Characters in brackets |
| [^ ] | Matches Characters NOT in brackets |
|   &#124;  | Either Or |
| ()   | Group |
| \*   | 0 or More |
| \+   | 1 or More |
| ?    | 0 or One |
| {3}  | Exact Number |
| {3,4}  | Range of Number (Minimum, Maximum) |

<br />
## Example1

### strings

    https://www.google.com

    http://coreyms.com

    https://youtube.com

    https://www.nasa.gov

### expression
    https?://(www\.)?(\w+)(\.\w+)


## Example2

### strings
    CoreyMSchafer@gmail.com
    corey.schafer@university.edu
    corey-321-schafer@my-work.net

### expression
    [a-zA-Z0-9.-]+@[a-zA-Z-]+\.(com|edu|net)
