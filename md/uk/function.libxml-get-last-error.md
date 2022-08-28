Вилучення останньої помилки з libxml

-   [« libxml\_get\_errors](function.libxml-get-errors.html)
    
-   [libxml\_set\_external\_entity\_loader »](function.libxml-set-external-entity-loader.html)
    
-   [PHP Manual](index.html)
    
-   [Функции libxml](ref.libxml.html)
    
-   Вилучення останньої помилки з libxml
    

# libxmlgetlasterror

(PHP 5> = 5.1.0, PHP 7, PHP 8)

libxmlgetlasterror — Вилучення останньої помилки з libxml

### Опис

```methodsynopsis
libxml_get_last_error(): LibXMLError|false
```

Вилучення останньої помилки з libxml.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [LibXMLError](class.libxmlerror.html)якщо в буфері є помилки, або **`false`** в іншому випадку.

### Дивіться також

-   [libxml\_get\_errors()](function.libxml-get-errors.html) - Отримання масиву помилок, що відбулися.
-   [libxml\_clear\_errors()](function.libxml-clear-errors.html) - Очищення буфера помилок libxml