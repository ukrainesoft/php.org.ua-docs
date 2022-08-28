Завершити коментар

-   [« XMLWriter::endCdata](xmlwriter.endcdata.html)
    
-   [XMLWriter::endDocument »](xmlwriter.enddocument.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити коментар
    

# XMLWriter::endComment

# xmlwriterendcomment

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::endComment -- xmlwriterendcomment — Завершити коментар

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::endComment(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_end_comment(XMLWriter $writer): bool
```

Завершує поточний коментар.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікували ресурс (resource). |

### Дивіться також

-   [XMLWriter::startComment()](xmlwriter.startcomment.html) - Створює стартовий коментар
-   [XMLWriter::writeComment()](xmlwriter.writecomment.html) - Записати повний тег коментаря