# The JRL Coding Standard

A place describing my personal coding standard in detail... perhaps in more detail than most would care about!

# Influences

* [JUCE Coding Standard](https://www.juce.com/learn/coding-standards)

# Language

## Encoding

Seeing that the code is intended to be used with all compilers, old and new, the code must be written in ASCII. Modern C++ compilers do support UTF-8 literals and even UTF-8 symbols in comments, but that does not always play nice with C++98 compilers.

## Spelling

Code must be written using [Canadian English](https://en.wikipedia.org/wiki/Canadian_English), favouring the British side of spelling.

### Suffixes

* `-our` as in _colour_, instead of _color_
* `-ise` as in _vectorise_, instead of _vectorize_
* `-tre` as in _centre_, instead of _center_

### Other Misc. Word Examples

* _travelling_ instead of _traveling_
* _grey_ instead of _gray_

# General Whitespace

* **No tabs**. Use 4 spaces
* Braces are [Allman style](https://en.wikipedia.org/wiki/Indent_style#Allman_style)

## Parenthese

Insert a single space before an open parenthesis, unless the pair of parentheses are empty.
```
void foo()
{
}

void foo (int a, int b)
{
}
```
