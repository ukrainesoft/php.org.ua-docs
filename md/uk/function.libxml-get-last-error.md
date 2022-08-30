Вилучення останньої помилки з libxml

-   [« libxmlgeterrors](function.libxml-get-errors.html)
    
-   [libxmlsetexternalentityloader »](function.libxml-set-external-entity-loader.html)
    
-   [PHP Manual](index.md)
    
-   [Функції libxml](ref.libxml.md)
    
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

Повертає об'єкт [LibXMLError](class.libxmlerror.md)якщо в буфері є помилки, або **`false`** в іншому випадку.

### Дивіться також

-   [libxmlgeterrors()](function.libxml-get-errors.html) - Отримання масиву помилок, що відбулися.
-   [libxmlclearerrors()](function.libxml-clear-errors.html) - Очищення буфера помилок libxml