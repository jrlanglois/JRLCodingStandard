# The JRL Coding Standard

A place describing my personal coding standard in detail... perhaps in more detail than most would care about!

# Influences

* [JUCE Coding Standard](https://www.juce.com/learn/coding-standards)

# Language

## Encoding

For all compilers, old and new, comments and code must be written in [ASCII](https://en.wikipedia.org/wiki/ASCII). There is no guarantee that a compiler will work fine with just any code page - some even throw warnings (e.g.: [Microsoft Visual Studio C4819](https://msdn.microsoft.com/en-us/library/ms173715.aspx))!

Put it this way: you definitely don't want to pick up source code and have to port it to an old compiler, only to have the pleasant waste of time of fixing encoding.

## Spelling

Comments and code must be written using [Canadian English](https://en.wikipedia.org/wiki/Canadian_English), favouring the British side of spelling.

### Suffixes

* `-our` as in _colour_, instead of _color_
* `-ise` as in _vectorise_, instead of _vectorize_
* `-tre` as in _centre_, instead of _center_

### Other Miscellaneous Word Examples

* _travelling_ instead of _traveling_
* _grey_ instead of _gray_

# General Whitespace

## Tabs vs Spaces

It's simple: **no tabs**. Instead, use 4 spaces.

The reasoning is to merely allow my particular formatting and placement styles.

## Braces

[Allman style](https://en.wikipedia.org/wiki/Indent_style#Allman_style)

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

_No_ - seriously, **no**. Disable it in your editor - you are careless if you don't.

You're throwing out consistent formatting when you bank on word wrapping, and make it difficult for others to read your code if they do not use that feature.

## Column Limitation

I am not a real fan of such a limit, but I do prefer keeping code within a half-window's space in an HD resolution view (as I typically have two code files open side-by-side).

If a group of lines are too long, it may indicate a higher-order breakdown; either by splitting the code into multiple lines, or even multiple functions!

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
