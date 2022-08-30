Завершити поточний елемент

-   [« XMLWriter::flush](xmlwriter.flush.html)
    
-   [XMLWriter::openMemory »](xmlwriter.openmemory.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Завершити поточний елемент
    

# XMLWriter::fullEndElement

# xmlwriterfullendelement

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL xmlwriter >= 2.0.4)

XMLWriter::fullEndElement -- xmlwriterfullendelement — Завершити поточний елемент

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::fullEndElement(): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_full_end_element(XMLWriter $writer): bool
```

Завершує поточний елемент XML. Записує тег, що закриває, навіть якщо елемент порожній.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endElement()](xmlwriter.endelement.html) - Завершити поточний елемент