Отримує від XML-аналізатора номер поточного стовпця

-   [« xml\_get\_current\_byte\_index](function.xml-get-current-byte-index.html)
    
-   [xml\_get\_current\_line\_number »](function.xml-get-current-line-number.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Отримує від XML-аналізатора номер поточного стовпця
    

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

Ця функція повертає **`false`**, якщо посилання параметра `parser` не веде до діючого аналізатора, або повертає номер стовпця на поточному рядку (визначеному за допомогою [xml\_get\_current\_line\_number()](function.xml-get-current-line-number.html)) згідно з поточним положенням покажчика аналізатора.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [xml\_get\_current\_byte\_index()](function.xml-get-current-byte-index.html) - Отримує поточний для XML-аналізатора байтовий індекс
-   [xml\_get\_current\_line\_number()](function.xml-get-current-line-number.html) - Отримує від XML-аналізатора номер поточного рядка