---
navigation:
  - function.odbc-connection-string-quote.md: « odbc\_connection\_string\_quote
  - function.odbc-cursor.md: odbc\_cursor »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_connection\_string\_should\_quote
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_connection\_string\_should\_quote

(PHP 8 >= 8.2.0)

odbc\_connection\_string\_should\_quote — Визначає, чи слід укладати значення рядка з'єднання ODBC у лапки

### Опис

```methodsynopsis
odbc_connection_string_should_quote(string $str): bool
```

Визначає, чи потрібно укладати рядок у лапки для рядкового значення з'єднання ODBC, тобто. містить вона спеціальні символи.

Зверніть увагу, що при цьому не перевіряється, чи укладено рядок у лапки; вже укладений у лапки рядок міститиме символи, які змусять цю функцію повернути значення true. Для перевірки слід використовувати функцію [odbc\_connection\_string\_is\_quoted()](function.odbc-connection-string-is-quoted.md)

### Список параметрів

`str`

Рядок, який необхідно перевірити.

### Значення, що повертаються

Повертає **`true`**, якщо рядок має бути поміщений у лапки, інакше повертає **`false`**

### Дивіться також

-   [odbc\_connection\_string\_quote()](function.odbc-connection-string-quote.md) \- Укладає в лапки значення рядка підключення
-   [odbc\_connection\_string\_is\_quoted()](function.odbc-connection-string-is-quoted.md) \- Визначає, чи встановлено значення рядка з'єднання ODBC у лапки
