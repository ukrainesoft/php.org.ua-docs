---
navigation:
  - function.odbc-connect.md: « odbc\_connect
  - function.odbc-connection-string-quote.md: odbc\_connection\_string\_quote »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_connection\_string\_is\_quoted
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_connection\_string\_is\_quoted

(PHP 8 >= 8.2.0)

odbc\_connection\_string\_is\_quoted — Визначає, чи встановлено значення рядка з'єднання ODBC у лапки.

### Опис

```methodsynopsis
odbc_connection_string_is_quoted(string $str): bool
```

Визначає, чи правильно укладено рядок у лапки для значення рядка з'єднання ODBC. Для лапок у рядку з'єднання ODBC використовуються фігурні дужки, причому завершальні дужки у рядку повинні бути екрановані шляхом повторення їх двічі, аналогічно лапкам у SQL.

### Список параметрів

`str`

Рядок, який необхідно перевірити на наявність лапок.

### Значення, що повертаються

Повертає **`true`**, якщо лапки наведені правильно, в іншому випадку повертає **`false`**

### Дивіться також

-   [odbc\_connection\_string\_quote()](function.odbc-connection-string-quote.md) \- Укладає в лапки значення рядка підключення
-   [odbc\_connection\_string\_should\_quote()](function.odbc-connection-string-should-quote.md) \- Визначає, чи слід укладати значення рядка з'єднання ODBC у лапки
