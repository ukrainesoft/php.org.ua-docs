Завершити поточний елемент

-   [« XMLWriter::endDtdEntity](xmlwriter.enddtdentity.md)
    
-   [XMLWriter::endPi »](xmlwriter.endpi.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                              |
|--------|-----------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElement()](xmlwriter.startelement.md) - Створити стартовий тег елемента
-   [XMLWriter::writeElement()](xmlwriter.writeelement.md) - Записати повний тег елемента