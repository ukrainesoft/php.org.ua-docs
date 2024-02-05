---
navigation:
  - ref.xml.md: « Функції парсера XML
  - function.xml-get-current-byte-index.md: xml\_get\_current\_byte\_index »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_error\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_error\_string

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_error\_string — Отримання рядка помилки XML-аналізатора

### Опис

```methodsynopsis
xml_error_string(int $error_code): ?string
```

Отримання рядкового подання помилки XML-аналізатора відповідно до переданого коду помилки `error_code`

### Список параметрів

`error_code`

Код помилки, що повертається функцією [xml\_get\_error\_code()](function.xml-get-error-code.md)

### Значення, що повертаються

Повертає рядок з текстовим описом коду помилки `error_code`или\*\*`null`\*\*, якщо опис не знайдено.

### Дивіться також

-   [xml\_get\_error\_code()](function.xml-get-error-code.md) \- Отримує код помилки XML-аналізатора
