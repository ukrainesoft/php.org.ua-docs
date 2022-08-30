Завершити поточний DTD

-   [« XMLWriter::endDocument](xmlwriter.enddocument.html)
    
-   [XMLWriter::endDtdAttlist »](xmlwriter.enddtdattlist.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточний DTD
    

# XMLWriter::endDtd

# xmlwriterenddtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtd -- xmlwriterenddtd — Завершити поточний DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtd(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd(XMLWriter $writer): bool
```

Завершує розділ визначення типу документа (DTD).

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

-   [XMLWriter::startDtd()](xmlwriter.startdtd.html) - Створити стартовий DTD тег
-   [XMLWriter::writeDtd()](xmlwriter.writedtd.html) - Записати повний тег DTD