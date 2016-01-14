# Линейный поиск в двумерном массиве. Временная сложность

```
def find_minimal(matrix, val):
    for i in range(len(matrix)):
        row = matrix[i]
        for j in range(len(row)):
            if cell == row[j]: //row[j] - элемент матрицы
                return (i, j)
```