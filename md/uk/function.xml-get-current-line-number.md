---
navigation:
  - function.xml-get-current-column-number.md: « xml\_get\_current\_column\_number
  - function.xml-get-error-code.md: xml\_get\_error\_code »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_get\_current\_line\_number
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_get\_current\_line\_number

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_get\_current\_line\_number — Отримує від XML-аналізатора номер поточного рядка

### Опис

```methodsynopsis
xml_get_current_line_number(XMLParser $parser): int
```

Отримує номер поточного рядка для заданого XML-аналізатора.

### Список параметрів

`parser`

Посилання на XML аналізатор для отримання номера рядка.

### Значення, що повертаються

Функція повертає номер рядка згідно з поточним положенням покажчика аналізатора.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Дивіться також

-   [xml\_get\_current\_column\_number()](function.xml-get-current-column-number.md) \- Отримує від XML-аналізатора номер поточного стовпця
-   [xml\_get\_current\_byte\_index()](function.xml-get-current-byte-index.md) \- Отримує поточний для XML-аналізатора байтовий індекс
