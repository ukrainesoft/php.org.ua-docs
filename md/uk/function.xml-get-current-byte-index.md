---
navigation:
  - function.xml-error-string.md: « xml\_error\_string
  - function.xml-get-current-column-number.md: xml\_get\_current\_column\_number »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_get\_current\_byte\_index
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_get\_current\_byte\_index

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_get\_current\_byte\_index — Отримує поточний для XML-аналізатора байтовий індекс

### Опис

```methodsynopsis
xml_get_current_byte_index(XMLParser $parser): int
```

Отримує поточний для заданого XML-аналізатора байтовий індекс.

### Список параметрів

`parser`

Посилання на XML-аналізатор, з якого буде отримано індекс байта.

### Значення, що повертаються

Функція повертає індекс байта в буфері даних аналізатора, де він перебуває у даний момент (починаючи з нуля).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Примітки

**Увага**

Ця функція повертає байтовий індекс, вважаючи, що текст закодовано UTF-8. Зміна кодування не вплине на виведення функції.

### Дивіться також

-   [xml\_get\_current\_column\_number()](function.xml-get-current-column-number.md) \- Отримує від XML-аналізатора номер поточного стовпця
-   [xml\_get\_current\_line\_number()](function.xml-get-current-line-number.md) \- Отримує від XML-аналізатора номер поточного рядка
