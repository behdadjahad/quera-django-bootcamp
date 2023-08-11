# Lecture 3 (14:00 to 15:30)

## regex

```python


regexStr = r"token-[0-9]+" # one or more digit after token-

regexStr = r"token-[0-9]*" # zero or more digit after token-

regexStr = r"token-[0-9]?" # zero or one digit after token-

regexStr = r"token-[0-9]{1,2}" # one or tow digit after token-

regexStr = r"token-[abcd]" # a, b, c, or d char after token-

regexStr = r"[+\-]?[0-9]" # this regex accept any integer number 


regexStr = r"[+\-]?[0-9]+\.[0-9]+" # this regex any float number


```

## linkes 

+ https://regex101.com/
+ https://regexr.com/


``` python
import re

my_regex = re.compile(r"[+\-]?[0-9]+\.[0-9]+",
                        re.IGNORECASE | re.MULTILINE)

text = "token-1234"

if my_regex.match(text):
    print("valid")
else:
    print("invalid")

```
