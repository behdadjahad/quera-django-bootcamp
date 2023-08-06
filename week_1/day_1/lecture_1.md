# Lecture 1 (10:00 to 11:30)

# python review

## simple print function

```python
print('hello, world')
```
the result will be:

```bash
user@ubuntu:~$ python3 print.py
user@ubuntu:~$ hello, world
user@ubuntu:~$
```

note: the print function will add new line at the end by default
use end parameter to set your custom ending char

```python
print('hello world', end='-')
```

```bash
user@ubuntu:~$ python3 print.py
user@ubuntu:~$ hello, world-user@ubuntu:~$
```

```python
print('hello world', end='-')
print('salam')
```

```bash
user@ubuntu:~$ hello, world-salam
user@ubuntu:~$
```


