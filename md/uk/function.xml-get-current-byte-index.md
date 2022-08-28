Отримує поточний для XML-аналізатора байтовий індекс

-   [« xml\_error\_string](function.xml-error-string.html)
    
-   [xml\_get\_current\_column\_number »](function.xml-get-current-column-number.html)
    
-   [PHP Manual](index.html)
    
-   [Функции парсера XML](ref.xml.html)
    
-   Отримує поточний для XML-аналізатора байтовий індекс
    

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

| Версия | Описание                                                                                                     |
|--------|--------------------------------------------------------------------------------------------------------------|
|        | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.html); раніше очікувався ресурс (resource). |

### Примітки

**Увага**

Ця функція повертає байтовий індекс, вважаючи, що текст закодовано UTF-8. Зміна кодування не вплине на виведення функції.

### Дивіться також

-   [xml\_get\_current\_column\_number()](function.xml-get-current-column-number.html) - Отримує від XML-аналізатора номер поточного стовпця
-   [xml\_get\_current\_line\_number()](function.xml-get-current-line-number.html) - Отримує від XML-аналізатора номер поточного рядка