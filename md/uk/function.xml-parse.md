Запускає аналіз XML-документа

-   [« xmlparseintostruct](function.xml-parse-into-struct.html)
    
-   [xmlparsercreatens »](function.xml-parser-create-ns.html)
    
-   [PHP Manual](index.md)
    
-   [Функции парсера XML](ref.xml.md)
    
-   Запускає аналіз XML-документа
    

# xmlparse

(PHP 4, PHP 5, PHP 7, PHP 8)

xmlparse — Запускає розбір документа XML

### Опис

```methodsynopsis
xml_parse(XMLParser $parser, string $data, bool $is_final = false): int
```

**xmlparse()** розбирає документ XML. Обробники запрограмованих подій викликаються стільки разів, скільки потрібно.

### Список параметрів

`parser`

Посилання на використовуваний XML-аналізатор.

`data`

Частина даних для аналізу. Документ можна розбирати частинами, викликаючи функцію **xmlparse()** кілька разів з новими даними, поки аргумент `is_final` не буде встановлений у **`true`**, Це повідомить аналізатору, що розуміється остання частина документа.

`is_final`

Якщо заданий та встановлений у **`true`** `data` вважається останньою частиною у цьому розборі.

### Значення, що повертаються

Повертає 1 при успішному завершенні, 0 інакше.

У разі невдалого аналізу інформацію про помилки можна отримати за допомогою функцій [xmlgeterrorcode()](function.xml-get-error-code.html) [xmlerrorstring()](function.xml-error-string.html) [xmlgetcurrentlinenumber()](function.xml-get-current-line-number.html) [xmlgetcurrentcolumnnumber()](function.xml-get-current-column-number.html) і [xmlgetcurrentbyteindex()](function.xml-get-current-byte-index.html)

> **Зауваження**
> 
> Деякі помилки (такі як помилки при розборі сутностей) видаються в кінці розбору і отримати їх можна тільки коли `is_final` встановлений в **`true`**

### список змін

| Версия | Описание                                                                                                   |
|--------|------------------------------------------------------------------------------------------------------------|
|        | Параметр `parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Розбір частин великих XML-документів**

Цей приклад показує, як великі XML-документи можуть бути прочитані та розібрані частинами, тому немає необхідності тримати весь документ у пам'яті. Обробка помилок опущена для стислості.

```php
<?php
$stream = fopen('large.xml', 'r');
$parser = xml_parser_create();
// установить обработчики
while (($data = fread($stream, 16384))) {
    xml_parse($parser, $data); // разобрать текущую часть
}
xml_parse($parser, '', true); // завершить разбор
xml_parser_free($parser);
fclose($stream);
```