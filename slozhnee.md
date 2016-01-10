# Сложнее

##16
Есть строка. Нужно получить новую строку, в которой после каждого слова, заканчивающегося на g, стоит знак «@».
```
def replacement(s):
    return s.replace("g ", "g@ ")
```
##17
Есть список чисел, нужно отобрать в новый список числа без повторов. 
```
def no_duplicates(arr):
    return list(set(arr))
```
##18
Отобрать из списка только уникальные элементы.
```
def unique_elements(arr):
    status = {}
    for n in arr:
        if n in status.keys():
            status[n] += 1
        else:
            status[n] = 1
    return [n for n in status if status[n] == 1]


x = [1, 2, 2, 2, 3, 3, 4, 4, 5, 6, 7, 8, 9, 10, 10]
print(unique_elements(x))
```
##19
Отобрать из списка неуникальные элементы.
```
def non_unique_elements(arr):
    status = {}
    for n in arr:
        if n in status.keys():
            status[n] += 1
        else:
            status[n] = 1
    return [n for n in status if status[n] > 1]


x = [1, 2, 2, 2, 3, 3, 4, 4, 4, 4, 4, 5, 6, 7, 8, 9, 10, 10]
print(non_unique_elements(x))
```
##20
Из массива (списка), содержащего 100 элементов выбрать 20 элементов в случайных неповторяющихся позициях. Переместить выбранные элементы в начало массива, обменяв их местами с имеющимися там.
##21
Отсортировать массив из 100 элементов по убыванию. Посчитать сумму всех нечетных элементов. Вычесть из каждого 3-го элемента данную сумму.
```
def happy_sorting(arr):
    sum_all = sum([n for n in arr if n % 2 == 1])
    for i in range(len(arr)):
        if i % 3 == 0:
            arr[i] -= sum_all
    return arr


x = [x for x in range(100)]
x = sorted(x)[::-1]
print(happy_sorting(x))
```
##22
В двумерном массиве найти строку массива, сумма элементов которой минимальна. Вычесть элементы данной строки из соответствующих элементов всех строк массива.
##23
Сгенерировать массив из 10 неповторяющихся элементов. Создать и двумерный массив 10*10 и скопировать элементы сгенерированного массива в каждую строку двумерного массива.
```
from random import sample

x = sample(range(100), 10)
matrix = [[None for j in range(10)] for i in range(10)]
for i in range(10):
    for j in range(10):
        matrix[i][j] = x[j]
print(matrix)
```
##24
Для массива 100 случайных чисел рассчитать среднеквадратическое отклонение. Вычесть из каждого элемента массива данное значение отклонения. Из результирующего массива выбрать 3 наибольших значения.
```
from random import randint
from math import sqrt

# Шаг 1
# Нужно создать массив из 100 случайных чисел
data = [randint(0,100) for i in range(100)]
print("data :", data, "\n")

# Шаг 2
# Нужно вычислить среднее арифметическое элементов массива
middle = sum(data) / 100
print("middle :", middle, "\n")

# Шаг 3
# Нужно вычислить среднее квадратичное отклонение
deviation = sqrt( sum( [ (x - middle)**2 for x in data ] ) / 100 )
deviation = round(deviation, 2) # округлим до 2-х знаков после запятой
print("deviation :", deviation, "\n")

# Шаг 4
# Из каждого элемента массива нужно вычесть среднее квадратичное отклонение
data = [round(x-deviation, 2) for x in data]
    # каждую полученную разность округлим до 2-х знаков после запятой
print("subtraction deviation :", data, "\n")

# Шаг 5
# В исходном массиве некоторые числа могут повторяться (потому что они случайные)
# Следовательно, в массиве, полученном после шага 4 также возможн повторения
# Так что из полученного списка необходимо исключить повторы
data = list(set(data))
print("without duplicates :", data, "\n")

# Шаг 6
# В полученном массиве нужно найти 3 наибольших значения
# Для этого нужно 3 раза подряд находить максимум и заносить его в отдельный массив
# После этого необходимо каждый раз удалять найденный максимум из массива, в котором он был найден
maximums = []
for i in range(3):
    max_number = max(data)
    maximums.append(max_number)
    data.remove(max_number)
print("maximums :", maximums)
```
##25
Создать два упорядоченных по возрастанию массива. Слить два массива в один также отсортированный по возрастанию.
```
from random import randint

a = sorted([randint(1, 100) for i in range(10)])
print(a)

b = sorted([randint(1, 100) for j in range(5)])
print(b)

c = sorted(a+b)
print(c)
```
##26
Сгенерировать два случайных массива размера 20 с неповторяющимися элементами в диапазоне от 0 до 100. Посчитать количество совпадений между элементами массивов.
```
from random import sample

a = sample(range(0, 100), 20)
print(a)

b = sample(range(0, 100), 20)
print(b)

counter = sum([1 for x in a if x in b])
print(counter)
```
##27
Сгенерировать два случайных двумерных массива одинакового размера. Перемножить элементы в соответствующих позициях и результат записать в третий
```
from random import randint

row = int(input("Enter number of strings: "))
col = int(input("Enter number of columns: "))

a = [[randint(1, 100) for j in range(col)] for i in range(row)]
print(a)

b = [[randint(1, 100) for j in range(col)] for i in range(row)]
print(b)

c = [[a[i][j]*b[i][j] for j in range(col)] for i in range(row)]
print(c)
```
##28
В двумерно массиве найти столбец, сумма элементов которого максимальна. Вычесть элементы этого столбца из соответствующих элементов остальных столбцов. Распечатать массив.
##29
Отсортировать двумерный массив алгоритмом пузырька.
```
from random import randint


def bubble_sorting(arr):
    for i in range(len(arr)-1, 0, -1):
        for j in range(i):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

data = [randint(1, 100) for i in range(10)]
print(data)
print(bubble_sorting(data))

```
##30
Отсортировать двумерный массив алгоритмом выбора