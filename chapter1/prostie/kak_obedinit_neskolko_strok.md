# Как объединить несколько строк.

Строки можно склеивать с помощью оператора +

```text
>>> str1 = 'Hello'
>>> str2 = 'World'
>>> str1 + ' ' + str2
'Hello World'
```

join – объединяет через разделитель набор строк:

```text
>>> seq = ['one','two','three']
>>> sep = ','
>>> sep.join(seq)
'one,two,three'
```

