# Поиск минимального(максимального) элемента в массиве. Временная сложность

Временная сложность n.

[Видео](http://www.youtube.com/watch?v=BXxYbLE09n4)

Реализация:

```
def find_minimal(lst):
    min = lst[0]
    for i in range(1, len(lst)):
        if lst[i] < min:
            min = lst[i]
    return min
```