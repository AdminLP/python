# Простые

**Осторожно, костыли!!! Лучше покинуть данную страницу и написать код самому\)\) Данные решения не есть достоверное и правильное решение. Это не тру вариант**

## 1

Есть строка. Нужно получить новую строку, в которой каждое новое слово начинается с большой буквы.

```text
str1 = 'hello world'
str2 = str1.title()
```

## 2

Есть строка. Нужно получить новую строку, в которой после каждого слова стоит восклицательный знак.

```text
str1 = 'hello world'
str2 = str1.replace(' ', '! ')+'!'
```

## 3

Есть строка. Необходимо посчитать количество слов в этой строке.

```text
str1 = 'hello world'
len(str1.split(' ')
```

## 4

Нужно получить строку из 1000 случайных чисел разделенных символом «+».

```text
from random import randint
str1 = ''
for number in range(1000):
    str1 += str(randint(1, 9)) + '+'
str1 = str1[:-1]
```

или

```text
from random import randint # Подключаем модуль для случайных чисел

# Нужно будет указать диапазон, из которого будут выбираться случайные числа
result = [str(randint(0,100)) for i in range(10)] # Воспользуемся генератором

print("+".join(result)) # Функция join = слияние элементов по разделителю
# Эта функция работает для строк - поэтому в генераторе использована функция str()
```

## 5

Есть список чисел. Необходимо найти наибольшее в правой части списка. В чем минус решения срезом.

```text
int_lst = [1, 2, 6, 8, 3, 5]
int_lst.reverse()
print(max(int_lst))
```

или

```text
def Right_Max(arr):
    result = max(arr[len(arr)//2::])
    return result
```

## 6

Есть список чисел. Нужно посчитать количество четных.

```text
int_lst = [1, 2, 6, 8, 3, 5]
counter = 0
for number in int_lst:
    if number % 2 == 0:
        counter += 1
print(counter)
```

или

```text
def Even_Number(arr):
    is_even = [1 for i in arr if i%2==0]
    number = sum(is_even)
    return number
```

## 7

Есть число. Нужно переставить цифры в обратном порядке.

```text
def reverse_integer(number):
    return int(str(number)[::-1])
```

## 8

Есть список чисел. Получить список с числами в обратном порядке.

```text
def reverse_integer(lst1):
    lst2 = []
    for number in lst1:
        lst2.append(int(str(number)[::-1]))
    return lst2
```

## 9

Описать словарем себя.

```text
about_me = {'name': 'Василий', 'surname': 'Крючков', 'years': 19, 'sex': 'муж.'}
```

или

```text
about_me = dict(name='Василий', surname='Крючков', years=19, sex='муж.')
```

## 10

Есть 2 списка. Нужно их объединить. extend

```text
lst1 = [1, 2, 3]
lst2 = ['sadf', 'qwer']
lst_extend = lst1+lst2
```

или

```text
def list_merge(lst1, lst2):
    for lst in lst2:
        lst1.append(lst)
    return lst1
```

или

```text
def Joining_Of_Lists(a,b):
    a.extend(b)
    return a
```

## 15

Есть список чисел. Необходимо получить список из квадратов этих чисел.

```text
lst1 = [1, 2, 3]
lst2 = [number ** 2 for number in lst1]
```

