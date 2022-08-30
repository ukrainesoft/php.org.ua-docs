Завершити поточний документ

-   [« XMLWriter::endComment](xmlwriter.endcomment.html)
    
-   [XMLWriter::endDtd »](xmlwriter.enddtd.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточний документ
    

# XMLWriter::endDocument

# xmlwriterenddocument

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::endDocument -- xmlwriterenddocument — Завершити поточний документ

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endDocument(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_document(XMLWriter $writer): bool
```

Завершує поточний документ.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                               |
|--------|------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startDocument()](xmlwriter.startdocument.html) - Створити тег документа