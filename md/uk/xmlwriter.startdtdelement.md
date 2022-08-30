Створити стартовий елемент DTD

-   [« XMLWriter::startDtdAttlist](xmlwriter.startdtdattlist.md)
    
-   [XMLWriter::startDtdEntity »](xmlwriter.startdtdentity.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
-   Створити стартовий елемент DTD
    

# XMLWriter::startDtdElement

# xmlwriterstartdtdelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startDtdElement -- xmlwriterstartdtdelement — Створити стартовий елемент DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startDtdElement(string $qualifiedName): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_dtd_element(XMLWriter $writer, string $qualifiedName): bool
```

Починає елемент DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

`qualifiedName`

Цілком визначене ім'я типу документа для створення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endDtdElement()](xmlwriter.enddtdelement.md) - Завершити поточний елемент DTD
-   [XMLWriter::writeDtdElement()](xmlwriter.writedtdelement.md) - Записати повний тег елемента DTD