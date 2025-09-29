## Strings exercise
Write a program capable of reading a string of characters (it can be simply in a variable, the input doesn't matter) and modifying it following the below instructions.

The first character *can* influence how the alphabetic characters will get transformed and the last character *can* influence how the numeric characters are transformed.

When the first character of the string is a:
- `$` "Encrypts" all alphabetic characters (a-z, A-Z), jumping two characters ahead (cyclic), for instance, 'A' becomes 'C', 'b' becomes 'd', 'K' becomes 'M' and 'Z' becomes 'B'
- `^` Converts all alphabetic characters into uppercase, 'a' becomes 'A', 'z' becomes 'Z', 'D' remains 'D'
- `_` Convert all aphabetic characters into lowercase, 'A' becomes 'a', 'Z' becomes 'z', 'd' remains 'd'

When the last character of the string is:
- `#` Converts each of the numeric characters (0-9) to the character 7
- `%` Converts each numeric character to 0 if it's pair, to 1 if it's even
- `/` Converts each of the numeric characters to itself, divided by 2, rounded up

Input - Output examples:
- 0000000# -> 7777777#
- $787878abc% => $101010cde%
- ^no_free_lunch -> ^NO_FREE_LUNCH
- _Utah_012345-Teapot/ -> _utah_011223-teapot/


Tips for solving the problem:<br>
(don't read if you think you can do it without them)<br><br>
Read about ascii table and latin, first 0 to 127 bits of the unicode table, character representation, how a string is stored in memory, every developer needs to know how characters and strings work (you will really learn that when you understand the different versions across languages + how they do memory allocation, too advanced for now), strings and chars are just so basic and essential for every field of programming, in the end, they are just numbers made of zeroes and ones mapped to their values, as if we had an array of 256 elements and just filled the 65th with an A, the 66th with a B and so on, if you wanna learn more, search about UTF-8, UTF-16 and "Characters, Symbols and the Unicode Miracle" (good Tom Scott youtube video about character encoding).


More material:

https://www.asciitable.com/
https://unicode-table.com/en/blocks/basic-latin
