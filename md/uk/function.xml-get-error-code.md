---
navigation:
  - function.xml-get-current-line-number.md: « xmlgetcurrentlinenumber
  - function.xml-parse-into-struct.md: xmlparseintostruct »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlgeterrorcode
---
# xmlgeterrorcode

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlgeterrorcode — Отримує код помилки XML-аналізатора

### Опис

```methodsynopsis
xml_get_error_code(XMLParser $parser): int
```

Отримує код помилки XML-аналізатора.

### Список параметрів

`parser`

Посилання на аналізатор XML для отримання коду помилки.

### Значення, що повертаються

Ця функція повертає **`false`**, якщо посилання параметра `parser` не веде до діючого аналізатора, або ж повертає один із кодів помилок зі списку, розташованого в [розділі кодів помилок](xml.error-codes.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [xmlerrorstring()](function.xml-error-string.md) - Отримання рядка помилки XML-аналізатора
