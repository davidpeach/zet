# Concatenate strings in bash

Thursday, 01 February 2024. 16:59:42GMT

There are different ways to concatenate strings in bash.

```bash
string_one="A B"
string_one+=" C"
echo "$string_one"

a="A"
b="B"
c="C"
string_two="${a} ${b} ${c}"
echo "$string_two"
```
