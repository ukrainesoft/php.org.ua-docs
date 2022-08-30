Порівняння рядків без урахування регістру з використанням алгоритму "natural order"

-   [« strlen](function.strlen.html)
    
-   [strnatcmp »](function.strnatcmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з рядками](ref.strings.html)
    
-   Порівняння рядків без урахування регістру з використанням алгоритму "natural order"
    

# strnatcasecmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strnatcasecmp — Порівняння рядків без урахування регістру за допомогою алгоритму "natural order"

### Опис

```methodsynopsis
strnatcasecmp(string $string1, string $string2): int
```

Ця функція реалізує алгоритм порівняння, який упорядковує алфавітно-цифрові рядки подібно до того, як це зробив би людина. Ця функція подібна [strnatcmp()](function.strnatcmp.html), крім того, що порівняння відбувається без урахування регістру символів. Для отримання додаткової інформації дивіться [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

### Значення, що повертаються

Подібно до інших функцій порівняння рядків, ця функція повертає від'ємне число, якщо `string1` менше `string2`, позитивне число, якщо `string1` більше `string2`, та 0, якщо рядки рівні.

### Приклади

**Приклад #1 Приклад використання **strnatcasecmp()****

```php
<?php

var_dump(strnatcasecmp('Apple', 'Banana'));
var_dump(strnatcasecmp('Banana', 'Apple'));
var_dump(strnatcasecmp('apple', 'Apple'));
?>
```

Результат виконання цього прикладу:

```
int(-1)
int(1)
int(0)
```

### Дивіться також

-   [pregmatch()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [strcmp()](function.strcmp.html) - Бінарно-безпечне порівняння рядків
-   [strcasecmp()](function.strcasecmp.html) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [substr()](function.substr.html) - Повертає підрядок
-   [stristr()](function.stristr.html) - Реєстронезалежний варіант функції strstr
-   [strncasecmp()](function.strncasecmp.html) - Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strncmp()](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.html) - Знаходить перше входження підрядка
-   [setlocale()](function.setlocale.html) - Встановлює налаштування локалі