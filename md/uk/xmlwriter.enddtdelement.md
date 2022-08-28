Завершити поточний елемент DTD

-   [« XMLWriter::endDtdAttlist](xmlwriter.enddtdattlist.html)
    
-   [XMLWriter::endDtdEntity »](xmlwriter.enddtdentity.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdElement()](xmlwriter.startdtdelement.html) - Створити стартовий елемент DTD
-   [XMLWriter::writeDtdElement()](xmlwriter.writedtdelement.html) - Записати повний тег елемента DTD