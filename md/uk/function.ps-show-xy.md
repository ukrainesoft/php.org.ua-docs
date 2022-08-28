Виводить текст у заданій позиції

-   [« ps\_show\_xy2](function.ps-show-xy2.html)
    
-   [ps\_show2 »](function.ps-show2.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Виводить текст у заданій позиції
    

# псshowзі

(PECL ps >= 1.1.0)

псshowxy — Виводить текст у заданій позиції

### Опис

```methodsynopsis
ps_show_xy(    resource $psdoc,    string $text,    float $x,    float $y): bool
```

Виводить текст у заданій текстовій позиції.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`text`

Текст для виведення.

`x`

Координата X лівого нижнього кута поля, що оточує текст.

`y`

Координата Y лівого нижнього кута поля навколишнього тексту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_continue\_text()](function.ps-continue-text.html) - Продовжує текст у наступному рядку
-   [ps\_show()](function.ps-show.html) - Виводить текст