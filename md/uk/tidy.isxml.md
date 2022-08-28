Визначає, чи документ є спільним XML-документом (не HTML/XHTML)

-   [« tidy::isXhtml](tidy.isxhtml.html)
    
-   [tidy::parseFile »](tidy.parsefile.html)
    
-   [PHP Manual](index.html)
    
-   [tidy](class.tidy.html)
    
-   Визначає, чи документ є спільним XML-документом (не HTML/XHTML)
    

# tidy::isXml

# tidyісxml

(PHP 5, PHP 7, PHP 8, PECL tidy> = 0.5.2)

tidy::isXml -- tidyісxml — Визначає, чи документ є спільним XML-документом (не HTML/XHTML)

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public tidy::isXml(): bool
```

Процедурний стиль

```methodsynopsis
tidy_is_xml(tidy $tidy): bool
```

Визначає, чи документ є спільним XML-документом (не HTML/XHTML).

### Список параметрів

`tidy`

Об'єкт [Tidy](class.tidy.html)

### Значення, що повертаються

Ця функція повертає **`true`**якщо зазначений tidy-об'єкт `tidy` є загальним XML-документом (не HTML/XHTML), або **`false`** в іншому випадку.

**Увага**

Ця функція ще не реалізована в самому Tidylib, тому завжди повертається **`false`**