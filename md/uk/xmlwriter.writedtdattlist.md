Записати повний тег DTD AttList

-   [« XMLWriter::writeDtd](xmlwriter.writedtd.md)
    
-   [XMLWriter::writeDtdElement »](xmlwriter.writedtdelement.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
-   Записати повний тег DTD AttList
    

# XMLWriter::writeDtdAttlist

# xmlwriterwritedtdattlist

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtdAttlist -- xmlwriterwritedtdattlist — Записати повний тег DTD AttList

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtdAttlist(string $name, string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd_attlist(XMLWriter $writer, string $name, string $content): bool
```

Записує атрибути DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`name`

Назва списку атрибутів DTD.

`content`

Вміст списку атрибутів DTD.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdAttlist()](xmlwriter.startdtdattlist.md) - Створює стартовий список атрибутів DTD
-   [XMLWriter::endDtdAttlist()](xmlwriter.enddtdattlist.md) - Завершити поточний список атрибутів DTD