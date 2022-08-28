Зберігає поточний контекст

-   [« ps\_rotate](function.ps-rotate.html)
    
-   [ps\_scale »](function.ps-scale.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Зберігає поточний контекст
    

# псsave

(PECL ps >= 1.1.0)

псsave — Зберігає поточний контекст

### Опис

```methodsynopsis
ps_save(resource $psdoc): bool
```

Зберігає поточний графічний контекст, що містить кольори, налаштування переміщення, повороту та багато іншого. Збережений контекст можна відновити за допомогою [ps\_restore()](function.ps-restore.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_restore()](function.ps-restore.html) - Відновлює раніше збережений контекст