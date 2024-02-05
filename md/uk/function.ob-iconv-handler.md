---
navigation:
  - function.iconv.md: « iconv
  - book.intl.md: intl »
  - index.md: PHP Manual
  - ref.iconv.md: Функції iconv
title: ob\_iconv\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_iconv\_handler

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

ob\_iconv\_handler — Перетворює символи з поточного кодування на кодування вихідного буфера

### Опис

```methodsynopsis
ob_iconv_handler(string $contents, int $status): string
```

Перетворює закодовану в `internal_encoding` рядок, у рядок, закодований у `output_encoding`

Значения`internal_encoding`и`output_encoding` повинні бути визначені у файлі php.ini чи функцією [iconv\_set\_encoding()](function.iconv-set-encoding.md)

### Список параметрів

Інформацію про аргументи цього обробника можна переглянути в описі функції [ob\_start()](function.ob-start.md)

### Значення, що повертаються

Інформацію про значення цього обробника, що повертаються, можна переглянути в описі до функції [ob\_start()](function.ob-start.md)

### Приклади

**Пример #1 Пример использования**ob\_iconv\_handler()\*\*\*\*

```php
<?php
iconv_set_encoding("internal_encoding", "UTF-8");
iconv_set_encoding("output_encoding", "ISO-8859-1");
ob_start("ob_iconv_handler"); // запуск буферизации вывода
?>
```

### Дивіться також

-   [iconv\_get\_encoding()](function.iconv-get-encoding.md) \- Отримує поточне значення налаштувань перетворення кодувань
-   [iconv\_set\_encoding()](function.iconv-set-encoding.md) \- Встановлює поточні налаштування для перетворення символів кодування
-   [Функції контролю виведення](ref.outcontrol.md)
