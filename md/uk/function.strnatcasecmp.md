---
navigation:
  - function.strlen.md: « strlen
  - function.strnatcmp.md: strnatcmp »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strnatcasecmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strnatcasecmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strnatcasecmp — Порівняння рядків без урахування регістру за допомогою алгоритму "natural order"

### Опис

```methodsynopsis
strnatcasecmp(string $string1, string $string2): int
```

Ця функція реалізує алгоритм порівняння, який упорядковує алфавітно-цифрові рядки подібно до того, як це зробив би людина. Ця функція подібна [strnatcmp()](function.strnatcmp.md), крім того, що порівняння відбувається без урахування регістру символів. Для отримання додаткової інформації дивіться [» Natural Order String Comparison](https://github.com/sourcefrog/natsort)

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

### Значення, що повертаються

Повертає `-1`, якщо `string1`меньше`string2` , якщо `string1`больше`string2`, и якщо рядки рівні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функція тепер повертає `-1`или ; раніше вона повертала негативне чи позитивне число. |

### Приклади

**Пример #1 Пример использования**strnatcasecmp()\*\*\*\*

```php
<?php

var_dump(strnatcasecmp('Apple', 'Banana'));
var_dump(strnatcasecmp('Banana', 'Apple'));
var_dump(strnatcasecmp('apple', 'Apple'));
?>
```

Результат виконання наведеного прикладу:

```
int(-1)
int(1)
int(0)
```

### Дивіться також

-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [strcmp()](function.strcmp.md) \- Бінарно-безпечне порівняння рядків
-   [strcasecmp()](function.strcasecmp.md) \- Бінарно-безпечне порівняння рядків без урахування регістру
-   [substr()](function.substr.md) \- Повертає підрядок
-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [strncasecmp()](function.strncasecmp.md) \- Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [strncmp()](function.strncmp.md) \- Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [setlocale()](function.setlocale.md) \- Встановлює налаштування локалі
