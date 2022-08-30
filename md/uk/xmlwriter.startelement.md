Створити стартовий тег елемента

-   [« XMLWriter::startDtdEntity](xmlwriter.startdtdentity.html)
    
-   [XMLWriter::startElementNs »](xmlwriter.startelementns.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити стартовий тег елемента
    

# XMLWriter::startElement

# xmlwriterstartelement

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startElement -- xmlwriterstartelement — Створити стартовий тег елемента

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startElement(string $name): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_element(XMLWriter $writer, string $name): bool
```

Починає елемент.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`name`

Ім'я елемент.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.html) - Завершити поточний елемент
-   [XMLWriter::writeElement()](xmlwriter.writeelement.html) - Записати повний тег елемента