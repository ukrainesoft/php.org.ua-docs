---
navigation:
  - function.error-clear-last.html: « errorclearlast
  - function.error-log.html: errorlog »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: errorgetlast
---
# errorgetlast

(PHP 5> = 5.2.0, PHP 7, PHP 8)

errorgetlast — Отримання інформації про останню помилку

### Опис

```methodsynopsis
error_get_last(): ?array
```

Отримує інформацію про останню помилку, що відбулася.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив з описом останньої помилки, що відбулася. Ключі масиву: "type", "message", "file" та "line". Якщо помилка відбулася у внутрішній функції PHP, елемент із ключем "message" почнеться з імені цієї функції. Повертає \*\*`null`\*\*якщо помилок ще не сталося.

### Приклади

**Приклад #1 Приклад використання **errorgetlast()****

```php
<?php
echo $a;
print_r(error_get_last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [type] => 8
    [message] => Undefined variable: a
    [file] => C:\WWW\index.php
    [line] => 2
)
```

### Дивіться також

-   [Константи помилок](errorfunc.constants.md)
-   Змінна [$phperrormsg](reserved.variables.phperrormsg.md)
-   [errorclearlast()](function.error-clear-last.html) - Очистити останню помилку
-   [Директива `display_errors`](errorfunc.configuration.html#ini.display-errors)
-   [Директива `html_errors`](errorfunc.configuration.html#ini.html-errors)
-   [Директива `xmlrpc_errors`](errorfunc.configuration.html#ini.xmlrpc-errors)
