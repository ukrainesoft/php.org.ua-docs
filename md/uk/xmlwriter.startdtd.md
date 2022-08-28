Створити стартовий DTD тег

-   [« XMLWriter::startDocument](xmlwriter.startdocument.html)
    
-   [XMLWriter::startDtdAttlist »](xmlwriter.startdtdattlist.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити стартовий DTD тег
    

# XMLWriter::startDtd

# xmlwriterstartdtd

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtd -- xmlwriterstartdtd - Створити стартовий DTD тег

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtd(string $qualifiedName, ?string $publicId = null, ?string $systemId = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd(    XMLWriter $writer,    string $qualifiedName,    ?string $publicId = null,    ?string $systemId = null): bool
```

Починає DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`qualifiedName`

Цілком визначене ім'я типу документа для створення.

`publicId`

Ідентифікатор зовнішнього громадського підмножини.

`systemId`

Ідентифікатор зовнішнього системного підмножини.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtd()](xmlwriter.enddtd.html) - Завершити поточний DTD
-   [XMLWriter::writeDtd()](xmlwriter.writedtd.html) - Записати повний тег DTD