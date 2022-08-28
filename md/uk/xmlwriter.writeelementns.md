Записати повний простір імен тега елемента

-   [« XMLWriter::writeElement](xmlwriter.writeelement.html)
    
-   [XMLWriter::writePi »](xmlwriter.writepi.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати повний простір імен тега елемента
    

# XMLWriter::writeElementNs

# xmlwriterwriteelementнс

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writeElementNs -- xmlwriterwriteelementns — Записати повний простір імен тега елемента

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writeElementNs(    ?string $prefix,    string $name,    ?string $namespace,    ?string $content = null): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_element_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace,    ?string $content = null): bool
```

Записує повний простір імен тега елемента.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`prefix`

Префікс простору імен. Якщо `prefix` дорівнює **`null`**, простір імен буде опущено.

`name`

Ім'я елемент.

`namespace`

URI простір імен. Якщо `namespace` дорівнює **`null`**, оголошення простору імен буде опущено.

`content`

Вміст елемента.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElementNs()](xmlwriter.startelementns.html) - Створити стартовий тег елемента простору імен
-   [XMLWriter::endElement()](xmlwriter.endelement.html) - Завершити поточний елемент
-   [XMLWriter::writeElement()](xmlwriter.writeelement.html) - Записати повний тег елемента