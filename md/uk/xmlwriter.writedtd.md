Записати повний тег DTD

-   [« XMLWriter::writeComment](xmlwriter.writecomment.html)
    
-   [XMLWriter::writeDtdAttlist »](xmlwriter.writedtdattlist.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний тег DTD
    

# XMLWriter::writeDtd

# xmlwriterwritedtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtd -- xmlwriterwritedtd — Записати повний тег DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtd(    string $name,    ?string $publicId = null,    ?string $systemId = null,    ?string $content = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd(    XMLWriter $writer,    string $name,    ?string $publicId = null,    ?string $systemId = null,    ?string $content = null): bool
```

Записує повний тег DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`name`

Ім'я DTD.

`publicId`

Ідентифікатор зовнішнього громадського підмножини.

`systemId`

Ідентифікатор зовнішнього системного підмножини.

`content`

Вміст DTD.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtd()](xmlwriter.startdtd.html) - Створити стартовий DTD тег
-   [XMLWriter::endDtd()](xmlwriter.enddtd.html) - Завершити поточний DTD