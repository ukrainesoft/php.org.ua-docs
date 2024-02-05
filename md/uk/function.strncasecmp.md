---
navigation:
  - function.strnatcmp.md: « strnatcmp
  - function.strncmp.md: strncmp »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strncasecmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strncasecmp

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

strncasecmp — Бінарно-безпечне порівняння перших n символів рядків без урахування регістру

### Опис

```methodsynopsis
strncasecmp(string $string1, string $string2, int $length): int
```

Ця функція схожа на [strcasecmp()](function.strcasecmp.md), за винятком того, що можна вказати максимальну кількість символів в обох рядках, які братимуть участь у порівнянні.

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

`length`

Кількість символів, що беруть участь у порівнянні.

### Значення, що повертаються

Повертає `-1`, якщо `string1`меньше`string2` , якщо `string1`больше`string2`, и якщо рядки рівні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функція тепер повертає `-1`или ; раніше вона повертала негативне чи позитивне число. |

### Приклади

**Пример #1 Пример использования**strncasecmp()\*\*\*\*

```php
<?php

$var1 = 'Hello John';
$var2 = 'hello Doe';
if (strncasecmp($var1, $var2, 5) === 0) {
    echo 'Первые 5 символов $var1 и $var2 равны при сравнении строк без учёта регистра';
}
?>
```

### Дивіться також

-   [strncmp()](function.strncmp.md) \- Бінарно-безпечне порівняння перших n символів рядків
-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [substr\_compare()](function.substr-compare.md) \- Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strcasecmp()](function.strcasecmp.md) \- Бінарно-безпечне порівняння рядків без урахування регістру
-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [substr()](function.substr.md) \- Повертає підрядок
