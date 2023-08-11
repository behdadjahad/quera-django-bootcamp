# Lecture 2 (12:00 to 13:30)

## multithread

```python
import threading

count = 10

def doFunc():
    for i in range(count):
        print('doFunc -> ' + str(i))


def doNewFunc():
    for i in range(count):
        print('doNewFunc -> ' + str(i))


doFunc()
doNewFunc()

print("@@@@@@@@@\n#######\n&&&&&&&")

t1  = threading.Thread(target=doFunc)
t2  = threading.Thread(target=doNewFunc)


t1.start()
t2.start()

```

https://en.wikipedia.org/wiki/Coroutine