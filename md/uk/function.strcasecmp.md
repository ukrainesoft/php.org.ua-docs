---
navigation:
  - function.str-word-count.html: « strwordcount
  - function.strchr.md: strchr »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strcasecmp
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

Повертає негативне число, якщо `string1` менше `string2`, позитивне число, якщо `string1` більше `string2`, та 0, якщо рядки рівні.

### Приклади

**Приклад #1 Приклад використання **strcasecmp()****

```php
<?php
$var1 = "Hello";
$var2 = "hello";
if (strcasecmp($var1, $var2) == 0) {
    echo '$var1 равно $var2 при сравнении без учёта регистра';
}
?>
```

### Дивіться також

-   [strcmp()](function.strcmp.md) - Бінарно-безпечне порівняння рядків
-   [pregmatch()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [substrcompare()](function.substr-compare.html) - Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strncasecmp()](function.strncasecmp.md) - Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
-   [stristr()](function.stristr.md) - Реєстронезалежний варіант функції strstr
-   [substr()](function.substr.md) - Повертає підрядок
