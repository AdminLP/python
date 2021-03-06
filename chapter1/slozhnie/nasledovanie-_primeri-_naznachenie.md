# Наследование, примеры, назначение

Наследование подразумевает то, что дочерний класс содержит все атрибуты родительского класса, при этом некоторые из них могут быть переопределены или добавлены в дочернем. Например, мы можем создать свой класс, похожий на словарь:

```text
>>> class Mydict(dict):
...     def get(self, key, default = 0):
...         return dict.get(self, key, default)
...
>>> a = dict(a=1, b=2)
>>> b = Mydict(a=1, b=2)
```

Класс Mydict ведёт себя точно так же, как и словарь, за исключением того, что метод get по умолчанию возвращает не None, а 0.

```text
>>> b['c'] = 4
>>> print(b)
{'a': 1, 'c': 4, 'b': 2}
>>> print(a.get('v'))
None
>>> print(b.get('v'))
0
```

