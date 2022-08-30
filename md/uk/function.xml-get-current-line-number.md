Отримує від XML-аналізатора номер поточного рядка

-   [« xmlgetcurrentcolumnnumber](function.xml-get-current-column-number.html)
    
-   [xmlgeterrorcode »](function.xml-get-error-code.html)
    
-   [PHP Manual](index.md)
    
-   [Функции парсера XML](ref.xml.md)
    
-   Отримує від XML-аналізатора номер поточного рядка
    

# xmlgetcurrentlinenumber

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlgetcurrentlinenumber — Отримує від XML-аналізатора номер поточного рядка

### Опис

```methodsynopsis
xml_get_current_line_number(XMLParser $parser): int
```

Отримує номер поточного рядка для заданого XML-аналізатора.

### Список параметрів

`parser`

Посилання на XML аналізатор для отримання номера рядка.

### Значення, що повертаються

Ця функція повертає **`false`**, якщо посилання параметра `parser` не веде до діючого аналізатора, або повертає номер рядка згідно з поточним положенням покажчика аналізатора.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [xmlgetcurrentcolumnnumber()](function.xml-get-current-column-number.html) - Отримує від XML-аналізатора номер поточного стовпця
-   [xmlgetcurrentbyteindex()](function.xml-get-current-byte-index.html) - Отримує поточний для XML-аналізатора байтовий індекс