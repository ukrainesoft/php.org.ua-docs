Визначає, чи є документ XHTML-документом

-   [« tidy::html](tidy.html.html)
    
-   [tidy::isXml »](tidy.isxml.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Визначає, чи є документ XHTML-документом
    

# tidy::isXhtml

# tidyісxhtml

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::isXhtml -- tidyісxhtml — Визначає, чи є документ XHTML-документом

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::isXhtml(): bool
```

Процедурний стиль

```methodsynopsis
tidy_is_xhtml(tidy $tidy): bool
```

Визначає, чи документ XHTML-документом.

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Функція повертає \*\*`true`\*\*якщо зазначений tidy-об'єкт `tidy` є XHTML-документом, або **`false`** в іншому випадку.

**Увага**

Ця функція ще не реалізована в самому Tidylib, тому завжди повертається **`false`**