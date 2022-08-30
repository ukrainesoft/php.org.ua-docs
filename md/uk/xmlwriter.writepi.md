Записати інструкцію обробки (PI)

-   [« XMLWriter::writeElementNs](xmlwriter.writeelementns.html)
    
-   [XMLWriter::writeRaw »](xmlwriter.writeraw.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Записати інструкцію обробки (PI)
    

# XMLWriter::writePi

# xmlwriterwriteпі

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::writePi -- xmlwriterwritepi — Записати інструкцію обробки (PI)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::writePi(string $target, string $content): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_write_pi(XMLWriter $writer, string $target, string $content): bool
```

Записує інструкцію обробки.

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriteropenuri()](xmlwriter.openuri.html) або [xmlwriteropenmemory()](xmlwriter.openmemory.html)

`target`

Ціль інструкції обробки.

`content`

Вміст інструкції обробки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::startPi()](xmlwriter.startpi.html) - Створити стартовий тег PI
-   [XMLWriter::endPi()](xmlwriter.endpi.html) - Закінчити поточну інструкцію обробки (PI)