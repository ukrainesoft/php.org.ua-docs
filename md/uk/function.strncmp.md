---
navigation:
  - function.strncasecmp.md: « strncasecmp
  - function.strpbrk.md: strpbrk »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strncmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strncmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strncmp - Бінарно-безпечне порівняння перших n символів рядків

### Опис

```methodsynopsis
strncmp(string $string1, string $string2, int $length): int
```

Ця функція схожа на [strcmp()](function.strcmp.md), за винятком того, що можна вказати максимальну кількість символів в обох рядках, які братимуть участь у порівнянні.

Ця функція враховує регістр символів.

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

`length`

Кількість символів, які у порівнянні.

### Значення, що повертаються

Повертає `-1`, якщо `string1`меньше`string2` , якщо `string1`больше`string2`, и якщо рядки рівні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функція тепер повертає `-1`или ; раніше вона повертала негативне чи позитивне число. |

### Приклади

**Приклад #1**strncmp()**example**

```php
<?php

$var1 = 'Hello John';
$var2 = 'Hello Doe';
if (strncmp($var1, $var2, 5) === 0) {
    echo 'Первые 5 символов $var1 и $var2 равны при сравнении строк с учётом регистра';
}
?>
```

### Дивіться також

-   [strncasecmp()](function.strncasecmp.md) \- Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [substr\_compare()](function.substr-compare.md) \- Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strcmp()](function.strcmp.md) \- Бінарно-безпечне порівняння рядків
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [substr()](function.substr.md) \- Повертає підрядок
