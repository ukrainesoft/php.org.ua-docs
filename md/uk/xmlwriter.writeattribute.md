Записати повний атрибут

-   [« XMLWriter::text](xmlwriter.text.html)
    
-   [XMLWriter::writeAttributeNs »](xmlwriter.writeattributens.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний атрибут
    

# XMLWriter::writeAttribute

# xmlwriterwriteattribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeAttribute -- xmlwriterwriteattribute — Записати повний атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeAttribute(string $name, string $value): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_attribute(XMLWriter $writer, string $name, string $value): bool
```

Записує повний атрибут.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`name`

Ім'я атрибуту.

`value`

Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Перемішування поделементів та атрибутів**

Якщо запис поделементів та атрибутів змішаний, будь-яка спроба запису атрибутів після першого поделемента завершиться помилкою і поверне false.

```php
<?php
$xml = new XMLWriter();
$xml->openMemory();

$xml->startElement('element');
$xml->writeAttribute('attr1', '0');
$xml->writeElement('subelem', '0');
var_dump($xml->writeAttribute('attr2', '0'));
$xml->endElement();

echo $xml->flush();
?>
```

Результат виконання цього прикладу:

```
bool(false)
<element attr1="0"><subelem>0</subelem></element>
```

### Дивіться також

-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.html) - Записати повний атрибут простору імен
-   [XMLWriter::startAttribute()](xmlwriter.startattribute.html) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.html) - Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.html) - Завершити атрибут