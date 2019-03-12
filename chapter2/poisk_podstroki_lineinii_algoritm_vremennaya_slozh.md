# Поиск подстроки. Линейный алгоритм. Временная сложность

```text
def find_substring(str, sub):
    pos = 0
    sub_len = len(sub)
    for i in range(len(str)):
        ch = str[i]
        if ch == sub[pos]:
            pos += 1
        else:
            pos = 0
        if pos == sub_len:
            return i - pos + 1
```

