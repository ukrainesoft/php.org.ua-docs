---
navigation:
  - function.xml-get-current-line-number.md: « xml\_get\_current\_line\_number
  - function.xml-parse-into-struct.md: xml\_parse\_into\_struct »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_get\_error\_code
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_get\_error\_code

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_get\_error\_code — Отримує код помилки XML-аналізатора

### Опис

```methodsynopsis
xml_get_error_code(XMLParser $parser): int
```

Отримує код помилки XML-аналізатора.

### Список параметрів

`parser`

Посилання на аналізатор XML для отримання коду помилки.

### Значення, що повертаються

Функція повертає один із кодів помилок зі списку, розташованого в [розділі кодів помилок](xml.error-codes.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Дивіться також

-   [xml\_error\_string()](function.xml-error-string.md) \- Отримання рядка помилки XML-аналізатора
