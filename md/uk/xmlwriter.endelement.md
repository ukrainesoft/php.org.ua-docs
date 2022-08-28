Завершити поточний елемент

-   [« XMLWriter::endDtdEntity](xmlwriter.enddtdentity.html)
    
-   [XMLWriter::endPi »](xmlwriter.endpi.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточний елемент
    

# XMLWriter::endElement

# xmlwriterendelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endElement -- xmlwriterendelement — Завершити поточний елемент

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endElement(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_element(XMLWriter $writer): bool
```

Завершує поточний елемент.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElement()](xmlwriter.startelement.html) - Створити стартовий тег елемента
-   [XMLWriter::writeElement()](xmlwriter.writeelement.html) - Записати повний тег елемента