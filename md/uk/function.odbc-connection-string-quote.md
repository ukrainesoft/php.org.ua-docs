---
navigation:
  - function.odbc-connection-string-is-quoted.md: « odbc\_connection\_string\_is\_quoted
  - function.odbc-connection-string-should-quote.md: odbc\_connection\_string\_should\_quote »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_connection\_string\_quote
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_connection\_string\_quote

(PHP 8 >= 8.2.0)

odbc\_connection\_string\_quote — Укладає в лапки значення рядка підключення

### Опис

```methodsynopsis
odbc_connection_string_quote(string $str): string
```

Вкладає в лапки значення рядка підключення відповідно до правил ODBC. Тобто воно буде оточене лапками, а всі фігурні дужки, що завершують, будуть екрановані. Це необхідно робити для всіх значень рядка підключення, які надходять від користувача. Невиконання цієї вимоги може призвести до проблем із розбором рядка підключення або ін'єкції значень у рядок підключення.

Зверніть увагу, що ця функція не перевіряє, чи вже не укладено рядок у лапки і чи не потребує вона лапок. Для цього слід використовувати функцію [odbc\_connection\_string\_is\_quoted()](function.odbc-connection-string-is-quoted.md) і [odbc\_connection\_string\_should\_quote()](function.odbc-connection-string-should-quote.md)

### Список параметрів

`str`

Рядок, не укладений у лапки.

### Значення, що повертаються

Повертає рядок, укладений у лапки, оточений фігурними дужками та правильно екранований.

### Приклади

**Пример #1 Пример использования**odbc\_connection\_string\_quote()\*\*\*\*

У цьому прикладі рядок полягає в лапки, а потім поміщається в рядок з'єднання. Зверніть увагу, що рядок укладено в лапки, а символ закінчення лапок у середині рядка був екранований.

```php
<?php
$value = odbc_connection_string_quote("foo}bar");
$connection_string = "DSN=PHP;UserValue=$value";
echo $connection_string;
?>
```

Висновок наведеного прикладу буде схожим на:

```
DSN=PHP;UserValue={foo}}bar}
```

### Дивіться також

-   [odbc\_connection\_string\_is\_quoted()](function.odbc-connection-string-is-quoted.md) \- Визначає, чи встановлено значення рядка з'єднання ODBC у лапки
-   [odbc\_connection\_string\_should\_quote()](function.odbc-connection-string-should-quote.md) \- Визначає, чи слід укладати значення рядка з'єднання ODBC у лапки
