Створити стартовий атрибут простору імен

-   [« XMLWriter::startAttribute](xmlwriter.startattribute.md)
    
-   [XMLWriter::startCdata »](xmlwriter.startcdata.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`prefix`

Префікс простору імен.

`name`

Ім'я атрибуту.

`namespace`

URI простір імен. Якщо `namespace` дорівнює **`null`**, оголошення простору імен буде опущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                              |
|--------|-----------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |
|        | `prefix` тепер допускає значення null.                                                                                |

### Дивіться також

-   [XMLWriter::startAttribute()](xmlwriter.startattribute.md) - Створити початковий атрибут
-   [XMLWriter::endAttribute()](xmlwriter.endattribute.md) - Завершити атрибут
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.md) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.md) - Записати повний атрибут простору імен