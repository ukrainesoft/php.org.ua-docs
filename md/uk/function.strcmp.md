---
navigation:
  - function.strchr.md: « strchr
  - function.strcoll.md: strcoll »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strcmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strcmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strcmp — Бінарно-безпечне порівняння рядків

### Опис

```methodsynopsis
strcmp(string $string1, string $string2): int
```

Ця функція враховує регістр символів.

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

**Приклад #1 Приклад використання** strcmp()\*\*\*\*

```php
<?php
$var1 = "Hello";
$var2 = "hello";
if (strcmp($var1, $var2) !== 0) {
    echo '$var1 не равно $var2 при регистрозависимом сравнении';
}
?>
```

### Дивіться також

-   [strcasecmp()](function.strcasecmp.md) \- Бінарно-безпечне порівняння рядків без урахування регістру
-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [substr\_compare()](function.substr-compare.md) \- Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strncmp()](function.strncmp.md) \- Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.md) \- Знаходить перше входження підрядка
-   [substr()](function.substr.md) \- Повертає підрядок
