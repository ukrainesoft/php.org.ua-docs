Записати повний простір імен тега елемента

-   [« XMLWriter::writeElement](xmlwriter.writeelement.md)
    
-   [XMLWriter::writePi »](xmlwriter.writepi.md)
    
-   [PHP Manual](index.md)
    
-   [XMLWriter](class.xmlwriter.md)
    
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

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.md). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.md) або [xmlwriteropenmemory()](xmlwriter.openmemory.md)

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

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.md); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startElementNs()](xmlwriter.startelementns.md) - Створити стартовий тег елемента простору імен
-   [XMLWriter::endElement()](xmlwriter.endelement.md) - Завершити поточний елемент
-   [XMLWriter::writeElement()](xmlwriter.writeelement.md) - Записати повний тег елемента