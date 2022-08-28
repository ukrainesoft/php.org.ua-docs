Продовжує текст у наступному рядку

-   [« ps\_closepath](function.ps-closepath.html)
    
-   [ps\_curveto »](function.ps-curveto.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Продовжує текст у наступному рядку
    

# псcontinuetext

(PECL ps >= 1.1.0)

псcontinuetext — Продовжує текст у наступному рядку

### Опис

```methodsynopsis
ps_continue_text(resource $psdoc, string $text): bool
```

Виводить текст на один рядок нижче останнього рядка. Міжрядковий інтервал береться зі значення "leading", яке має бути встановлене за допомогою [ps\_set\_value()](function.ps-set-value.html). Фактичне положення тексту визначається значеннями "text" та "text", які можна запросити за допомогою функції [ps\_get\_value()](function.ps-get-value.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.html)

`text`

Текст для виведення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_show()](function.ps-show.html) - Виводить текст
-   [ps\_show\_xy()](function.ps-show-xy.html) - Виводить текст у заданій позиції
-   [ps\_show\_boxed()](function.ps-show-boxed.html) - Виводить текст у поле