Бінарно-безпечне порівняння рядків

-   [« strchr](function.strchr.html)
    
-   [strcoll »](function.strcoll.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Бінарно-безпечне порівняння рядків
    

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

-   [strcasecmp()](function.strcasecmp.html) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [preg\_match()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [substr\_compare()](function.substr-compare.html) - Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strncmp()](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків
-   [strstr()](function.strstr.html) - Знаходить перше входження підрядка
-   [substr()](function.substr.html) - Повертає підрядок