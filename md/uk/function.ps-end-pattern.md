Завершує шаблон

-   [« ps\_end\_page](function.ps-end-page.html)
    
-   [ps\_end\_template »](function.ps-end-template.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Завершує шаблон
    

# псendpattern

(PECL ps >= 1.2.0)

псendpattern — Завершує шаблон

### Опис

```methodsynopsis
ps_end_pattern(resource $psdoc): bool
```

Завершує шаблон, який було розпочато з [ps\_begin\_pattern()](function.ps-begin-pattern.html). Коли шаблон закінчено, його можна використовувати як колір заливки областей.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_begin\_pattern()](function.ps-begin-pattern.html) - Починає новий візерунок