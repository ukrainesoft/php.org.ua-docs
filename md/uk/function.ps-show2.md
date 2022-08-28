Виводить текст у поточній позиції

-   [« ps\_show\_xy](function.ps-show-xy.html)
    
-   [ps\_show »](function.ps-show.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Виводить текст у поточній позиції
    

# псshow2

(PECL ps >= 1.1.0)

псshow2 — Виводить текст у поточній позиції

### Опис

```methodsynopsis
ps_show2(resource $psdoc, string $text, int $len): bool
```

Виводить текст у поточній позиції. Не виводить більше `len` символів.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`text`

Текст для виведення.

`len`

Максимальна кількість символів для виведення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.