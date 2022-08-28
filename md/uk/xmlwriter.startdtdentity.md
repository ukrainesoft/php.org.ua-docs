Створити стартовий запис DTD

-   [« XMLWriter::startDtdElement](xmlwriter.startdtdelement.html)
    
-   [XMLWriter::startElement »](xmlwriter.startelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити стартовий запис DTD
    

# XMLWriter::startDtdEntity

# xmlwriterstartdtdentity

(PHP 5 >= 5.2.1, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdEntity - xmlwriterstartdtdentity — Створити стартовий запис DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtdEntity(string $name, bool $isParam): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd_entity(XMLWriter $writer, string $name, bool $isParam): bool
```

Починає записування DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`name`

Назва запису.

`isParam`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdEntity()](xmlwriter.enddtdentity.html) - Завершити поточний запис DTD
-   [XMLWriter::writeDtdEntity()](xmlwriter.writedtdentity.html) - Записати повний тег DTD запису