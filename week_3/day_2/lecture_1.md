# lecture 1 (10:00 - 11:30)


## vnev

```console
$ python3 -m venv test

```

some files and folders are created

```console
$ cd test
$ cat pyvenv.cfg
```

```ini

home = C:\Users\www.markazi.co\AppData\Local\Programs\Python\Python310
include-system-site-packages = false
version = 3.10.6

```

activation script for windows
```
> test\Scripts\activate
```
activation script for linux or mac
``` console
$ source test/bin/activate
```


creating requirements file
``` console
pip freeze > requirements.txt
```

deactivate command
``` console
$ deactivate
```

+ using venv in vscode 