Завершити атрибут

-   [« XMLWriter](class.xmlwriter.html)
    
-   [XMLWriter::endCdata »](xmlwriter.endcdata.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити атрибут
    

# XMLWriter::endAttribute

# xmlwriterendattribute

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endAttribute -- xmlwriterendattribute — Завершити атрибут

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endAttribute(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_attribute(XMLWriter $writer): bool
```

Завершує поточний атрибут.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startAttribute()](xmlwriter.startattribute.html) - Створити початковий атрибут
-   [XMLWriter::startAttributeNs()](xmlwriter.startattributens.html) - Створити стартовий атрибут простору імен
-   [XMLWriter::writeAttribute()](xmlwriter.writeattribute.html) - Записати повний атрибут
-   [XMLWriter::writeAttributeNs()](xmlwriter.writeattributens.html) - Записати повний атрибут простору імен