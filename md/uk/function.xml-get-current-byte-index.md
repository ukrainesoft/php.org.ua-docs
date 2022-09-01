---
navigation:
  - function.xml-error-string.html: « xmlerrorstring
  - function.xml-get-current-column-number.html: xmlgetcurrentcolumnnumber »
  - index.md: PHP Manual
  - ref.xml.md: Функции парсера XML
title: xmlgetcurrentbyteindex
---
# xmlgetcurrentbyteindex

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlgetcurrentbyteindex — Отримує поточний для XML-аналізатора байтовий індекс

### Опис

```methodsynopsis
xml_get_current_byte_index(XMLParser $parser): int
```

Отримує поточний для заданого XML-аналізатора байтовий індекс.

### Список параметрів

`parser`

Посилання на XML-аналізатор, з якого буде отримано індекс байта.

### Значення, що повертаються

Ця функція поверне **`false`**, якщо аргумент `parser` не посилається на припустимий аналізатор, інакше вона повертає індекс байта в буфері даних аналізатора, у якому він у даний момент (починаючи з нуля).

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |

### Примітки

**Увага**

Ця функція повертає байтовий індекс, вважаючи, що текст закодовано UTF-8. Зміна кодування не вплине на виведення функції.

### Дивіться також

-   [xmlgetcurrentcolumnnumber()](function.xml-get-current-column-number.md) - Отримує від XML-аналізатора номер поточного стовпця
-   [xmlgetcurrentlinenumber()](function.xml-get-current-line-number.md) - Отримує від XML-аналізатора номер поточного рядка
