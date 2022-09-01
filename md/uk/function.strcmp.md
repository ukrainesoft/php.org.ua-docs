---
navigation:
  - function.strchr.html: « strchr
  - function.strcoll.html: strcoll »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: strcmp
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

Повертає негативне число, якщо `string1` менше `string2`, позитивне число, якщо `string1` більше `string2`, та 0, якщо рядки рівні.

### Приклади

**Приклад #1 Приклад використання **strcmp()****

```php
<?php
$var1 = "Hello";
$var2 = "hello";
if (strcmp($var1, $var2) !== 0) {
    echo '$var1 не равно $var2 при регистрозависимом сравнении';
}
?>
```

### Дивіться також

-   [strcasecmp()](function.strcasecmp.md) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [pregmatch()](function.preg-match.md) - Виконує перевірку на відповідність регулярному виразу
-   [substrcompare()](function.substr-compare.md) - Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strncmp()](function.strncmp.md) - Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.md) - Знаходить перше входження підрядка
-   [substr()](function.substr.md) - Повертає підрядок
