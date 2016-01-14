# Линейный поиск в массиве. Временная сложность

Временная сложность O(n).

[Видео](https://www.youtube.com/watch?v=7S4XqXpivfY)

Реализация

```
def linear_search(lst, val):
    for i in range(lst):
        if lst[i] == val:
            return i
    return None

```