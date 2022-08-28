Перевірити, чи є параметр параметром зі змінною кількістю аргументів

-   [« ReflectionParameter::isPassedByReference](reflectionparameter.ispassedbyreference.html)
    
-   [ReflectionParameter::\_\_toString »](reflectionparameter.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionParameter](class.reflectionparameter.html)
    
-   Перевірити, чи є параметр параметром зі змінною кількістю аргументів
    

# ReflectionParameter::isVariadic

(PHP 5> = 5.6.0, PHP 7, PHP 8)

ReflectionParameter::isVariadic — Перевірити, чи є параметр параметром зі змінною кількістю аргументів

### Опис

```methodsynopsis
public ReflectionParameter::isVariadic(): bool
```

Перевіряє, чи визначено параметр як [параметр с переменным числом аргументов](functions.arguments.html#functions.variable-arg-list)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо параметр приймає змінну кількість аргументів, **`false`** в іншому випадку.