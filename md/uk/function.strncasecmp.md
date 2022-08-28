Бінарно-безпечне порівняння перших n символів рядків без урахування регістру

-   [« strnatcmp](function.strnatcmp.html)
    
-   [strncmp »](function.strncmp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Бінарно-безпечне порівняння перших n символів рядків без урахування регістру
    

# strncasecmp

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

strncasecmp — Бінарно-безпечне порівняння перших n символів рядків без урахування регістру

### Опис

```methodsynopsis
strncasecmp(string $string1, string $string2, int $length): int
```

Ця функція схожа на [strcasecmp()](function.strcasecmp.html), за винятком того, що можна вказати максимальну кількість символів в обох рядках, які братимуть участь у порівнянні.

### Список параметрів

`string1`

Перший рядок.

`string2`

Другий рядок.

`length`

Кількість символів, що беруть участь у порівнянні.

### Значення, що повертаються

Повертає негативне число, якщо `string1` менше `string2`, позитивне число, якщо `string1` більше `string2`, та 0, якщо рядки рівні.

### Приклади

**Приклад #1 Приклад використання **strncasecmp()****

```php
<?php

$var1 = 'Hello John';
$var2 = 'hello Doe';
if (strncasecmp($var1, $var2, 5) === 0) {
    echo 'Первые 5 символов $var1 и $var2 равны при сравнении строк без учёта регистра';
}
?>
```

### Дивіться також

-   [strncmp()](function.strncmp.html) - Бінарно-безпечне порівняння перших n символів рядків
-   [preg\_match()](function.preg-match.html) - Виконує перевірку на відповідність регулярному виразу
-   [substr\_compare()](function.substr-compare.html) - Бінарно-безпечне порівняння 2 рядків зі зміщенням, з урахуванням або без обліку регістру
-   [strcasecmp()](function.strcasecmp.html) - Бінарно-безпечне порівняння рядків без урахування регістру
-   [stristr()](function.stristr.html) - Реєстронезалежний варіант функції strstr
-   [substr()](function.substr.html) - Повертає підрядок