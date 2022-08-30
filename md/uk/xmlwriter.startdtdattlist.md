Створює стартовий список атрибутів DTD

-   [« XMLWriter::startDtd](xmlwriter.startdtd.md)
    
-   [XMLWriter::startDtdElement »](xmlwriter.startdtdelement.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Назва списку атрибутів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                             |
|--------|----------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdAttlist()](xmlwriter.enddtdattlist.md) - Завершити поточний список атрибутів DTD
-   [XMLWriter::writeDtdAttlist()](xmlwriter.writedtdattlist.md) - Записати повний тег DTD AttList