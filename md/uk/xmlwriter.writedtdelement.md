Записати повний тег елемента DTD

-   [« XMLWriter::writeDtdAttlist](xmlwriter.writedtdattlist.html)
    
-   [XMLWriter::writeDtdEntity »](xmlwriter.writedtdentity.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний тег елемента DTD
    

# XMLWriter::writeDtdElement

# xmlwriterwritedtdelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeDtdElement -- xmlwriterwritedtdelement — Записати повний тег елемента DTD

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeDtdElement(string $name, string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_dtd_element(XMLWriter $writer, string $name, string $content): bool
```

Записує повний тег елемента DTD.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`name`

Назва елемента DTD.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDtdElement()](xmlwriter.startdtdelement.html) - Створити стартовий елемент DTD
-   [XMLWriter::endDtdElement()](xmlwriter.enddtdelement.html) - Завершити поточний елемент DTD