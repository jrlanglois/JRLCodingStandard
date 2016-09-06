# The JRL Coding Standard

A place describing my personal coding standard in detail... perhaps in more detail than most would care about!

Note that the coding standard may be C/C++ biased, but I intend to have it generalised enough to apply to any C-like language.

# Influences

* [JUCE Coding Standard](https://www.juce.com/learn/coding-standards)

# Language

## Encoding

For all compilers, old and new, comments and code must be written in [ASCII](https://en.wikipedia.org/wiki/ASCII). There is no guarantee that a compiler will work fine with just any code page - some even throw warnings! (e.g.: [Microsoft Visual Studio C4819](https://msdn.microsoft.com/en-us/library/ms173715.aspx))

### Reasoning 

You definitely don't want to pick up source code and have to port it to an old compiler, only to waste time fixing encoding.

## Spelling

Comments and code must be written using [Canadian English](https://en.wikipedia.org/wiki/Canadian_English), favouring the British side of spelling.

### Suffixes

* `-our` as in _colour_, instead of _color_
* `-ise` as in _vectorise_, instead of _vectorize_
* `-tre` as in _centre_, instead of _center_

### Other Miscellaneous Word Examples

* _travelling_ instead of _traveling_
* _grey_ instead of _gray_

# Documentation

Use [Doxygen](https://www.stack.nl/~dimitri/doxygen/manual/commands.html), with the `@` symbol for commands.

Do not redundantly specify default commands.

For example, do this to automatically make use of `@brief`:
```
/** Does stuff and things */
void foo();
```

# General Whitespace

## Tabs vs Spaces

It's simple: **no tabs**. Instead, use 4 spaces.

### Reasoning 

To allow for my particular formatting and placement styles, and enforcing consistency across all software.

## Braces

[Allman style](https://en.wikipedia.org/wiki/Indent_style#Allman_style), where curly brackets are on a separate line.

```
int foo()
{
    if (somethingHappened())
    {
        static int foo = 0;
        ++foo;
        return foo;
    }

    return 0;
}
```

## Word Wrapping

_No_ - seriously, **no**. Disable it in your editor.

### Reasoning

You're throwing out consistent formatting when you bank on word wrapping, and make it difficult for others to read your code if they do not use that feature.

The goal is to have all of the precious text you spend your valuable time on looking the exact same, no matter where you bring it.

## Column Limitation

I am not a real fan of such a limit, but I do prefer keeping code within a half-window's space in an HD resolution view (as I typically have two code files open side-by-side).

If a group of lines are too long, it may indicate a higher-order breakdown; by splitting the code into multiple lines,   multiple functions, etc...

## Parentheses

Insert a single space before an open parenthesis, unless the pair of parentheses are empty.
```
void foo()
{
}

void foo (int a, int b)
{
}
```
