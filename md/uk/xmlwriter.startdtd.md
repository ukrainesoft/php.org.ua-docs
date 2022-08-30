Створити стартовий DTD тег

-   [« XMLWriter::startDocument](xmlwriter.startdocument.md)
    
-   [XMLWriter::startDtdAttlist »](xmlwriter.startdtdattlist.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

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
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtd()](xmlwriter.enddtd.md) - Завершити поточний DTD
-   [XMLWriter::writeDtd()](xmlwriter.writedtd.md) - Записати повний тег DTD