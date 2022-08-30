Записати повний тег DTD запису

-   [« XMLWriter::writeDtdElement](xmlwriter.writedtdelement.html)
    
-   [XMLWriter::writeElement »](xmlwriter.writeelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний тег DTD запису
    

# XMLWriter::writeDtdEntity

# xmlwriterwritedtdentity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtdEntity -- xmlwriterwritedtdentity — Записати повний тег DTD запису

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtdEntity(    string $name,    string $content,    bool $isParam = false,    ?string $publicId = null,    ?string $systemId = null,    ?string $notationData = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd_entity(    XMLWriter $writer,    string $name,    string $content,    bool $isParam = false,    ?string $publicId = null,    ?string $systemId = null,    ?string $notationData = null): bool
```

Записує повний запис DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`name`

Назва запису.

`content`

Вміст запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |
|  | `publicId` `systemId` і `notationData` тепер допускають значення null. |

### Дивіться також

-   [XMLWriter::startDtdEntity()](xmlwriter.startdtdentity.html) - Створити стартовий запис DTD
-   [XMLWriter::endDtdEntity()](xmlwriter.enddtdentity.html) - Завершити поточний запис DTD