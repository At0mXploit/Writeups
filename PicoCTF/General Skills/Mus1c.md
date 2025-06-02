# Solution

This song has the very slight scent of a programming language, and indeed, searching for ["shout" "put" programming language](https://www.google.com/search?q=%22shout%22+%22put%22+programming+language) brings us to a language called [Rockstar](https://codewithrockstar.com/).

> Rockstar is a computer programming language designed for creating programs that are also hair metal power ballads.

Pasting the program into the [online interpreter](https://codewithrockstar.com/online), we get the following output:

```
114
114
114
111
99
107
110
114
110
48
49
49
51
114
```

This looks like ASCII, let's decode it:

```python
>>> ascii = """114
... 114
... 114
... 111
... 99
... 107
... 110
... 114
... 110
... 48
... 49
... 49
... 51
... 114
... """
>>> for c in ascii.split():
...     print(chr(int(c)), end='')
...
rrrocknrn0113r
>>>
```


- `picoCTF{rrrocknrn0113r}`

---
