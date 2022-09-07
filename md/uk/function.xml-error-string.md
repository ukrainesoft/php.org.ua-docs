---
navigation:
  - ref.xml.md: « Функции парсера XML
  - function.xml-get-current-byte-index.md: xmlgetcurrentbyteindex »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlerrorstring
---
# xmlerrorstring

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlerrorstring — Отримання рядка помилки XML-аналізатора

### Опис

```methodsynopsis
xml_error_string(int $error_code): ?string
```

Отримання рядкового подання помилки XML-аналізатора відповідно до переданого коду помилки `error_code`

### Список параметрів

`error_code`

Код помилки, що повертається функцією [xmlgeterrorcode()](function.xml-get-error-code.md)

### Значення, що повертаються

Повертає рядок з текстовим описом коду помилки `error_code` або **`null`**, якщо опис не знайдено.

### Дивіться також

-   [xmlgeterrorcode()](function.xml-get-error-code.md) - Отримує код помилки XML-аналізатора
