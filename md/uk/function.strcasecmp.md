---
navigation:
  - function.str-word-count.md: « str\_word\_count
  - function.strchr.md: strchr »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strcasecmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# strcasecmp

(PHP 4, PHP 5, PHP 7, PHP 8)

strcasecmp — Бінарно-безпечне порівняння рядків без урахування регістру

### Опис

```methodsynopsis
strcasecmp(string $string1, string $string2): int
```

Бінарно-безпечне порівняння рядків без урахування регістру. Порівняння залежить від локалі; лише літери ASCII порівнюються без урахування регістру.

### Список параметрів

`string1`

Перший рядок

`string2`

Другий рядок

### Значення, що повертаються

Повертає `-1`, якщо `string1`меньше`string2` , якщо `string1`больше`string2`, и якщо рядки рівні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Функція тепер повертає `-1`или ; раніше вона повертала негативне чи позитивне число. |

### Приклади

**Пример #1 Пример использования**strcasecmp()\*\*\*\*

```php
<?php
$var1 = "Hello";
$var2 = "hello";
if (strcasecmp($var1, $var2) == 0) {
    echo '$var1 равно $var2 при сравнении без учёта регистра';
}
?>
```

### Дивіться також

-   [strcmp()](function.strcmp.md) \- Бінарно-безпечне порівняння рядків
-   [preg\_match()](function.preg-match.md) \- Виконує перевірку на відповідність регулярному виразу
-   [substr\_compare()](function.substr-compare.md) \- Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strncasecmp()](function.strncasecmp.md) \- Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [stristr()](function.stristr.md) \- Реєстронезалежний варіант функції strstr
-   [substr()](function.substr.md) \- Повертає підрядок
