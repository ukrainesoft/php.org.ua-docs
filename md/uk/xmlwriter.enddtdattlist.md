Завершити поточний список атрибутів DTD

-   [« XMLWriter::endDtd](xmlwriter.enddtd.html)
    
-   [XMLWriter::endDtdElement »](xmlwriter.enddtdelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточний список атрибутів DTD
    

# XMLWriter::endDtdAttlist

# xmlwriterenddtdattlist

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdAttlist -- xmlwriterenddtdattlist — Завершити поточний список атрибутів DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtdAttlist(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd_attlist(XMLWriter $writer): bool
```

Завершує поточний список атрибутів DTD документа.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdAttlist()](xmlwriter.startdtdattlist.html) - Створює стартовий список атрибутів DTD
-   [XMLWriter::writeDtdAttlist()](xmlwriter.writedtdattlist.html) - Записати повний тег DTD AttList