---
navigation:
  - function.error-clear-last.md: « error\_clear\_last
  - function.error-log.md: error\_log »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: error\_get\_last
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# error\_get\_last

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

error\_get\_last — Отримання інформації про останню помилку

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

**Приклад #1 Приклад використання** error\_get\_last()\*\*\*\*

```php
<?php
echo $a;
print_r(error_get_last());
?>
```

Висновок наведеного прикладу буде схожим на:

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
-   Переменная[$php\_errormsg](reserved.variables.phperrormsg.md)
-   [error\_clear\_last()](function.error-clear-last.md) \- Очистити останню помилку
-   [Директива`display_errors`](errorfunc.configuration.md#ini.display-errors)
-   [Директива`html_errors`](errorfunc.configuration.md#ini.md-errors)
-   [Директива`xmlrpc_errors`](errorfunc.configuration.md#ini.xmlrpc-errors)
