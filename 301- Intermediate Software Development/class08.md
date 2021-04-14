# Regexr

  Regular expressions (regex or regexp) are extremely useful in extracting information from any text by searching for one or more matches of a specific search pattern (i.e. a specific sequence of ASCII or unicode characters).

```

## Anchors —  ^ and $

^The        matches any string that starts with The -> Try it!
end$        matches a string that ends with end
^The end$   exact string match (starts and ends with The end)
roar        matches any string that has the text roar in it

## Quantifiers — * + ? and {}

abc*        matches a string that has ab followed by zero or more c
abc+        matches a string that has ab followed by one or more c
abc?        matches a string that has ab followed by zero or one c
abc{2}      matches a string that has ab followed by 2 c
abc{2,}     matches a string that has ab followed by 2 or more c
abc{2,5}    matches a string that has ab followed by 2 up to 5 c
a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc

## OR operator — | or []

a(b|c)     matches a string that has a followed by b or c (and captures b or c) 
a[bc]      same as previous, but without capturing b or c
Character classes — \d \w \s and .
\d         matches a single character that is a digit
\w         matches a word character (alphanumeric character plus underscore) 
\s         matches a whitespace character (includes tabs and line breaks)
.          matches any character. 