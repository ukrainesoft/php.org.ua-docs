Створює стартовий список атрибутів DTD

-   [« XMLWriter::startDtd](xmlwriter.startdtd.html)
    
-   [XMLWriter::startDtdElement »](xmlwriter.startdtdelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створює стартовий список атрибутів DTD
    

# XMLWriter::startDtdAttlist

# xmlwriterstartdtdattlist

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdAttlist -- xmlwriterstartdtdattlist — Створення стартового списку атрибутів DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtdAttlist(string $name): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd_attlist(XMLWriter $writer, string $name): bool
```

Починає перелік атрибутів DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`name`

Назва списку атрибутів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdAttlist()](xmlwriter.enddtdattlist.html) - Завершити поточний список атрибутів DTD
-   [XMLWriter::writeDtdAttlist()](xmlwriter.writedtdattlist.html) - Записати повний тег DTD AttList