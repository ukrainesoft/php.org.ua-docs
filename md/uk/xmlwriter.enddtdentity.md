Завершити поточний запис DTD

-   [« XMLWriter::endDtdElement](xmlwriter.enddtdelement.html)
    
-   [XMLWriter::endElement »](xmlwriter.endelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточний запис DTD
    

# XMLWriter::endDtdEntity

# xmlwriterenddtdentity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdEntity -- xmlwriterenddtdentity — Завершити поточний запис DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtdEntity(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd_entity(XMLWriter $writer): bool
```

Завершує поточний запис DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdEntity()](xmlwriter.startdtdentity.html) - Створити стартовий запис DTD
-   [XMLWriter::writeDtdEntity()](xmlwriter.writedtdentity.html) - Записати повний тег DTD запису