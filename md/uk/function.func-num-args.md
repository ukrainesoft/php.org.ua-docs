---
navigation:
  - function.func-get-args.md: « func\_get\_args
  - function.function-exists.md: function\_exists »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: func\_num\_args
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# func\_num\_args

(PHP 4, PHP 5, PHP 7, PHP 8)

func\_num\_args - Повертає кількість аргументів, переданих функції

### Опис

```methodsynopsis
func_num_args(): int
```

Отримує кількість аргументів переданих функції.

Ця функція також може бути використана спільно з [func\_get\_arg()](function.func-get-arg.md) і [func\_get\_args()](function.func-get-args.md) для створення функцій із змінною кількістю аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість аргументів, переданих поточній функції користувача.

### Помилки

Генерує попередження під час виклику поза визначенням функції.

### Приклади

**Приклад #1 Приклад використання** func\_num\_args()\*\*\*\*

```php
<?php

function foo()
{
    echo "Количество аргументов: ", func_num_args(), PHP_EOL;
}

foo(1, 2, 3);
?>
```

Результат виконання наведеного прикладу:

```
Количество аргументов: 3
```

### Примітки

> **Зауваження** :
> 
> Починаючи з PHP 8.0.0 сімейство функцій func\_\*() призначено для більшої прозорості щодо іменованих аргументів, обробляючи аргументи так, ніби всі вони були передані позиційно, а відсутні аргументи замінюються їх значеннями за умовчанням. Функція ігнорує набір невідомих варіативних аргументів. До зібраних невідомих іменованих аргументів можна отримати доступ лише через варіативний параметр.

### Дивіться також

-   [Синтаксис`...`](functions.arguments.md#functions.variable-arg-list)
-   [func\_get\_arg()](function.func-get-arg.md)
-   [func\_get\_args()](function.func-get-args.md)
-   [ReflectionFunctionAbstract::getNumberOfParameters()](reflectionfunctionabstract.getnumberofparameters.md)
