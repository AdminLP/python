# Алгоритм бинарного поиска. Временная сложность

[Видео](http://www.youtube.com/watch?v=R_aZdj4vtFI)

Временная сложность log\(n\).

```text
def qsort(lst):
    if len(lst) <= 1:
        return lst
    mid = lst[len(lst) // 2]
    left = []
    right = []
    eq = []
    for num in s:
        if num < mid:
            left.append(num)
        elif num > min:
            right.append(num)
        else:
            eq.append(num)
    return qsort(left) + eq + qsort(right)
```

