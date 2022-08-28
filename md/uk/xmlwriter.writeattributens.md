Записати повний атрибут простору імен

-   [« XMLWriter::writeAttribute](xmlwriter.writeattribute.html)
    
-   [XMLWriter::writeCdata »](xmlwriter.writecdata.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний атрибут простору імен
    

# XMLWriter::writeAttributeNs

# xmlwriterwriteattributeнс

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeAttributeNs -- xmlwriterwriteattributens — Записати повний атрибут простору імен

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeAttributeNs(    ?string $prefix,    string $name,    ?string $namespace,    string $value): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_attribute_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace,    string $value): bool
```

Записує повний атрибут простору імен.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`prefix`

Префікс простору імен. Якщо `prefix` дорівнює **`null`**, простір імен буде опущено.

`name`

Ім'я атрибуту.

`namespace`

URI простір імен. Якщо `namespace` дорівнює **`null`**, оголошення простору імен буде опущено.

`content`

Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.html) - Записати повний атрибут
-   [XMLWriter::startAttribute()](xmlwriter.startattribute.html) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.html) - Створити стартовий атрибут простору імен
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.html) - Завершити атрибут