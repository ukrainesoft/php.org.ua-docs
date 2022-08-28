Отримує код помилки XML-аналізатора

-   [« xml\_get\_current\_line\_number](function.xml-get-current-line-number.html)
    
-   [xml\_parse\_into\_struct »](function.xml-parse-into-struct.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Отримує код помилки XML-аналізатора
    

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

Ця функція повертає **`false`**, якщо посилання параметра `parser` не веде до діючого аналізатора, або ж повертає один із кодів помилок зі списку, розташованого в [разделе кодов ошибок](xml.error-codes.html)

### список змін

| Версия | Описание                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------|
|        | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [xml\_error\_string()](function.xml-error-string.html) - Отримання рядка помилки XML-аналізатора