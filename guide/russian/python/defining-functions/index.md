---
title: Python Defining Functions
localeTitle: Функции определения Python
---
[Документы Python](https://docs.python.org/3/tutorial/controlflow.html#defining-functions)

Мы можем создать функцию, которая записывает ряд Фибоначчи в произвольную границу:
```
>>> def fib(n):    # write Fibonacci series up to n 
 ...     """Print a Fibonacci series up to n.""" 
 ...     a, b = 0, 1 
 ...     while a < n: 
 ...         print(a, end=' ') 
 ...         a, b = b, a+b 
 ...     print() 
 ... 
 >>> # Now call the function we just defined: 
 ... fib(2000) 
 0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987 1597 
```

Ключевое слово [`def`](https://docs.python.org/3/reference/compound_stmts.html#def) вводит определение функции. За ним должно следовать имя функции и список формальных параметров в скобках. Операторы, которые образуют тело функции, начинаются со следующей строки и должны быть отступом.

Первый оператор тела функции может быть произвольным строковым литералом; этот строковый литерал является строкой документации функции или [docstring](https://www.python.org/dev/peps/pep-0257/) (больше о docstrings можно найти в разделе «Строки документации»). Некоторые инструменты используют docstrings для автоматического создания онлайн-или печатной документации или для интерактивного просмотра пользователем кода. Хорошая практика заключается в том, чтобы включить в текст код, который вы пишете, поэтому попробуйте сделать его привычкой.