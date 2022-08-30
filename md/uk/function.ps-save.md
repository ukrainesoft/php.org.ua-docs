Зберігає поточний контекст

-   [«psrotate](function.ps-rotate.html)
    
-   [псscale »](function.ps-scale.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Зберігає поточний контекст
    

# псsave

(PECL ps >= 1.1.0)

псsave — Зберігає поточний контекст

### Опис

```methodsynopsis
ps_save(resource $psdoc): bool
```

Зберігає поточний графічний контекст, що містить кольори, налаштування переміщення, повороту та багато іншого. Збережений контекст можна відновити за допомогою [псrestore()](function.ps-restore.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псrestore()](function.ps-restore.html) - Відновлює раніше збережений контекст