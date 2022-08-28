Записати повний тег елемента

-   [« XMLWriter::writeDtdEntity](xmlwriter.writedtdentity.html)
    
-   [XMLWriter::writeElementNs »](xmlwriter.writeelementns.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний тег елемента
    

# XMLWriter::writeElement

# xmlwriterwriteelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeElement -- xmlwriterwriteelement — Записати повний тег елемента

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeElement(string $name, ?string $content = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_element(XMLWriter $writer, string $name, ?string $content = null): bool
```

Записує повний тег елемент.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`name`

Ім'я елемент.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElement()](xmlwriter.startelement.html) - Створити стартовий тег елемента
-   [XMLWriter::endElement()](xmlwriter.endelement.html) - Завершити поточний елемент
-   [XMLWriter::writeElementNs()](xmlwriter.writeelementns.html) - Записати повний простір імен тега елемента