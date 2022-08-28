Виводить гліф

-   [« ps\_symbol\_width](function.ps-symbol-width.html)
    
-   [ps\_translate »](function.ps-translate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Виводить гліф
    

# псsymbol

(PECL ps >= 1.2.0)

псsymbol - Виводить гліф

### Опис

```methodsynopsis
ps_symbol(resource $psdoc, int $ord): bool
```

Виводить гліф у позиції `ord` у векторному кодування поточного шрифту. Кодування шрифту можна встановити під час завантаження шрифту за допомогою [ps\_findfont()](function.ps-findfont.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`ord`

Положення гліфа у векторному шрифт кодування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_symbol\_name()](function.ps-symbol-name.html) - Отримує ім'я гліфа
-   [ps\_symbol\_width()](function.ps-symbol-width.html) - Отримує ширину гліфа