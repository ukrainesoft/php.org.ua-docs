Створити стартовий атрибут простору імен

-   [« XMLWriter::startAttribute](xmlwriter.startattribute.html)
    
-   [XMLWriter::startCdata »](xmlwriter.startcdata.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити стартовий атрибут простору імен
    

# XMLWriter::startAttributeNs

# xmlwriterstartattributeнс

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startAttributeNs -- xmlwriterstartattributens — Створити стартовий атрибут простору імен

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startAttributeNs(?string $prefix, string $name, ?string $namespace): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_attribute_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace): bool
```

Починає атрибут простору імен.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`prefix`

Префікс простору імен.

`name`

Ім'я атрибуту.

`namespace`

URI простір імен. Якщо `namespace` дорівнює **`null`**, оголошення простору імен буде опущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |
|        | `prefix` тепер допускає значення null.                                                                                  |

### Дивіться також

-   [XMLWriter::startAttribute()](xmlwriter.startattribute.html) - Створити початковий атрибут
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.html) - Завершити атрибут
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.html) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.html) - Записати повний атрибут простору імен