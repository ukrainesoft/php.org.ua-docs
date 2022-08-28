Завершує шаблон

-   [« ps\_end\_pattern](function.ps-end-pattern.html)
    
-   [ps\_fill\_stroke »](function.ps-fill-stroke.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Завершує шаблон
    

# псendtemplate

(PECL ps >= 1.2.0)

псendtemplate — Завершує шаблон

### Опис

```methodsynopsis
ps_end_template(resource $psdoc): bool
```

Завершує шаблон, який було розпочато за допомогою [ps\_begin\_template()](function.ps-begin-template.html). Після завершення шаблону його можна використовувати як зображення.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_begin\_template()](function.ps-begin-template.html) - Починає новий шаблон