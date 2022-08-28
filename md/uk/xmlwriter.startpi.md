Створити стартовий тег PI

-   [« XMLWriter::startElementNs](xmlwriter.startelementns.html)
    
-   [XMLWriter::text »](xmlwriter.text.html)
    
-   [PHP Manual](index.html)
    
-   [XMLWriter](class.xmlwriter.html)
    
-   Створити стартовий тег PI
    

# XMLWriter::startPi

# xmlwriterstartпі

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL xmlwriter >= 0.1.0)

XMLWriter::startPi -- xmlwriterstartpi — Створити стартовий тег PI

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public XMLWriter::startPi(string $target): bool
```

Процедурний стиль

```methodsynopsis
xmlwriter_start_pi(XMLWriter $writer, string $target): bool
```

Починає тег інструкції з обробки (PI).

### Список параметрів

`writer`

Тільки для процедурних дзвінків. Змінний екземпляр [XMLWriter](class.xmlwriter.html). Об'єкт повертається з дзвінка [xmlwriter\_open\_uri()](xmlwriter.openuri.html) або [xmlwriter\_open\_memory()](xmlwriter.openmemory.html)

`target`

Ціль інструкції обробки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                |
|--------|-------------------------------------------------------------------------------------------------------------------------|
|        | У параметрі `writer` тепер очікується екземпляр [XMLWriter](class.xmlwriter.html); раніше очікувався ресурс (resource). |

### Дивіться також

-   [XMLWriter::endPi()](xmlwriter.endpi.html) - Закінчити поточну інструкцію обробки (PI)
-   [XMLWriter::writePi()](xmlwriter.writepi.html) - Записати інструкцію обробки (PI)