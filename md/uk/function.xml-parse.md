---
navigation:
  - function.xml-parse-into-struct.md: « xml\_parse\_into\_struct
  - function.xml-parser-create-ns.md: xml\_parser\_create\_ns »
  - index.md: PHP Manual
  - ref.xml.md: Функції парсера XML
title: xml\_parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xml\_parse

(PHP 4, PHP 5, PHP 7, PHP 8)

xml\_parse — Запускає розбір документа XML

### Опис

```methodsynopsis
xml_parse(XMLParser $parser, string $data, bool $is_final = false): int
```

**xml\_parse()** розбирає документ XML. Обробники запрограмованих подій викликаються стільки разів, скільки потрібно.

### Список параметрів

`parser`

Посилання на використовуваний XML-аналізатор.

`data`

Частина даних для аналізу. Документ можна розбирати частинами, викликаючи функцію **xml\_parse()** кілька разів з новими даними, поки аргумент `is_final`не будет установлен в\*\*`true`\*\*, Це повідомить аналізатору, що розуміється остання частина документа.

`is_final`

Якщо заданий та встановлений у **`true`** `data` вважається останньою частиною у цьому розборі.

### Значення, що повертаються

Повертає 1 при успішному завершенні, 0 інакше.

У разі невдалого аналізу інформацію про помилки можна отримати за допомогою функцій [xml\_get\_error\_code()](function.xml-get-error-code.md) [xml\_error\_string()](function.xml-error-string.md) [xml\_get\_current\_line\_number()](function.xml-get-current-line-number.md) [xml\_get\_current\_column\_number()](function.xml-get-current-column-number.md) і [xml\_get\_current\_byte\_index()](function.xml-get-current-byte-index.md)

> **Зауваження** :
> 
> Деякі помилки (такі як помилки при розборі сутностей) видаються в кінці розбору і отримати їх можна тільки коли `is_final`установлен в\*\*`true`\*\*

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`parser` чекає на екземпляр [XMLParser](class.xmlparser.md); раніше очікувався коректний `xml` ресурс (Resource). |

### Приклади

**Приклад #1 Розбір частин великих XML-документів**

Цей приклад показує, як великі XML-документи можуть бути прочитані та розібрані частинами, тому немає необхідності тримати весь документ у пам'яті. Обробка помилок опущена для стислості.

```php
<?php
$stream = fopen('large.xml', 'r');
$parser = xml_parser_create();
// установить обработчики
while (($data = fread($stream, 16384))) {
    xml_parse($parser, $data); // разобрать текущую часть
}
xml_parse($parser, '', true); // завершить разбор
xml_parser_free($parser);
fclose($stream);
```
