Створити стартовий тег елемента простору імен

-   [« XMLWriter::startElement](xmlwriter.startelement.html)
    
-   [XMLWriter::startPi »](xmlwriter.startpi.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити стартовий тег елемента простору імен
    

# XMLWriter::startElementNs

# xmlwriterstartelementнс

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startElementNs -- xmlwriterstartelementns — Створити стартовий тег елемента простору імен

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startElementNs(?string $prefix, string $name, ?string $namespace): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_element_ns(    XMLWriter $writer,    ?string $prefix,    string $name,    ?string $namespace): bool
```

Починає елемент простору імен.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`prefix`

Префікс простору імен. Якщо `prefix` дорівнює **`null`**, простір імен буде опущено.

`name`

Ім'я елемент.

`namespace`

URI простір імен. Якщо `namespace` дорівнює **`null`**, оголошення простору імен буде опущено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.html) - Завершити поточний елемент
-   [XMLWriter::writeElementNs()](xmlwriter.writeelementns.html) - Записати повний простір імен тега елемента