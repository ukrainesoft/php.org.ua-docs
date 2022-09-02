---
navigation:
  - function.xml-get-current-byte-index.md: « xmlgetcurrentbyteindex
  - function.xml-get-current-line-number.md: xmlgetcurrentlinenumber »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlgetcurrentcolumnnumber
---
# xmlgetcurrentcolumnnumber

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlgetcurrentcolumnnumber — Отримує від XML-аналізатора номер поточного стовпця

### Опис

```methodsynopsis
xml_get_current_column_number(XMLParser $parser): int
```

Отримує поточний номер стовпця заданого XML-аналізатора.

### Список параметрів

`parser`

Посилання на XML аналізатор для отримання номера стовпця.

### Значення, що повертаються

Ця функція повертає **`false`**, якщо посилання параметра `parser` не веде до діючого аналізатора, або повертає номер стовпця на поточному рядку (визначеному за допомогою [xmlgetcurrentlinenumber()](function.xml-get-current-line-number.md)) згідно з поточним положенням покажчика аналізатора.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [xmlgetcurrentbyteindex()](function.xml-get-current-byte-index.md) - Отримує поточний для XML-аналізатора байтовий індекс
-   [xmlgetcurrentlinenumber()](function.xml-get-current-line-number.md) - Отримує від XML-аналізатора номер поточного рядка
