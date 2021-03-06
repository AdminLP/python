# Что такое кортеж, примеры, назначение

Кортежи \(англ. tuple\) используется для представления неизменяемой последовательности разнородных объектов. Они обычно записываются в круглых скобках, но если неоднозначности не возникает, то скобки можно опустить.

```text
>>> t = (2, 2.05, "Hello")
>>> t
(2, 2.0499999999999998, 'Hello')
>>> (a, b, c) = t
>>> print a, b, c
2 2.05 Hello
>>> z, y, x = t
>>> print z, y, x
2 2.05 Hello
>>> a=1
>>> b=2
>>> a,b=b,a
>>> print a,b
2 1
>>> x = 12,
>>> x
(12,)
```

Как видно из примера, кортеж может быть использован и в левой части оператора присваивания. Значения из кортежа в левой части оператора присваивания связываются с аналогичными элементами правой части. Этот факт как раз и дает нам такие замечательные возможности как массовая инициализация переменных и возврат множества значений из функции одновременно. Последний пример демонстрирует создание кортежа из одного элмента \(его часто называют синглтоном\).

