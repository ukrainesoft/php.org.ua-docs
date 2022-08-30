Скинути поточний буфер

-   [« XMLWriter::endPi](xmlwriter.endpi.html)
    
-   [XMLWriter::fullEndElement »](xmlwriter.fullendelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Скинути поточний буфер
    

# XMLWriter::flush

# xmlwriterflush

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 1.0.0)

XMLWriter::flush -- xmlwriterflush — Скинути поточний буфер

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::flush(bool $empty = true): string|int
```

Процедурний стиль

```methodsynopsis
xmlwriter_flush(XMLWriter $writer, bool $empty = true): string|int
```

Скидає поточний буфер.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`empty`

Визначає, чи звільнити буфер чи ні. За замовчуванням **`true`**

### Значення, що повертаються

Якщо XML створюється в пам'яті, функція поверне згенерований буфер XML, інакше, при використанні URI, ця функція запише буфер і поверне кількість записаних байт.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |
|  | Функція більше не може повертати **`false`** |