Отримання рядка помилки XML-аналізатора

-   [« Функции парсера XML](ref.xml.html)
    
-   [xml\_get\_current\_byte\_index »](function.xml-get-current-byte-index.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Отримання рядка помилки XML-аналізатора
    

# xmlerrorstring

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlerrorstring — Отримання рядка помилки XML-аналізатора

### Опис

```methodsynopsis
xml_error_string(int $error_code): ?string
```

Отримання рядкового подання помилки XML-аналізатора відповідно до переданого коду помилки `error_code`

### Список параметрів

`error_code`

Код помилки, що повертається функцією [xml\_get\_error\_code()](function.xml-get-error-code.html)

### Значення, що повертаються

Повертає рядок з текстовим описом коду помилки `error_code` або **`null`**, якщо опис не знайдено.

### Дивіться також

-   [xml\_get\_error\_code()](function.xml-get-error-code.html) - Отримує код помилки XML-аналізатора