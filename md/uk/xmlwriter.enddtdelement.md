Завершити поточний елемент DTD

-   [« XMLWriter::endDtdAttlist](xmlwriter.enddtdattlist.md)
    
-   [XMLWriter::endDtdEntity »](xmlwriter.enddtdentity.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
-   Завершити поточний елемент DTD
    

# XMLWriter::endDtdElement

# xmlwriterenddtdelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDtdElement -- xmlwriterenddtdelement — Завершити поточний елемент DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDtdElement(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_dtd_element(XMLWriter $writer): bool
```

Завершує поточний елемент DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                              |
|--------|-----------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdElement()](xmlwriter.startdtdelement.md) - Створити стартовий елемент DTD
-   [XMLWriter::writeDtdElement()](xmlwriter.writedtdelement.md) - Записати повний тег елемента DTD