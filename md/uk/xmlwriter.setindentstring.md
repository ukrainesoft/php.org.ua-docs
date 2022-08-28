Встановити рядок, який використовується для відступів

-   [« XMLWriter::setIndent](xmlwriter.setindent.html)
    
-   [XMLWriter::startAttribute »](xmlwriter.startattribute.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Встановити рядок, який використовується для відступів
    

# XMLWriter::setIndentString

# xmlwritersetindentstring

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::setIndentString -- xmlwritersetindentstring — Встановити рядок, який використовується для відступів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::setIndentString(string $indentation): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_set_indent_string(XMLWriter $writer, string $indentation): bool
```

Встановлює рядок, який буде використовуватися для відступу кожного елемента/атрибута в XML.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`indentString`

Відступ рядка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Примітки

> **Зауваження**
> 
> Відступ скидається при відкритті xmlwriter.

### Дивіться також

-   [XMLWriter::setIndent()](xmlwriter.setindent.html) - Увімкнути або вимкнути відступи