Відновлює раніше збережений контекст

-   [« ps\_rect](function.ps-rect.html)
    
-   [ps\_rotate »](function.ps-rotate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Відновлює раніше збережений контекст
    

# псrestore

(PECL ps >= 1.1.0)

псrestore — Відновлює раніше збережений контекст

### Опис

```methodsynopsis
ps_restore(resource $psdoc): bool
```

Відновлює раніше збережений графічний контекст. Будь-який виклик [ps\_save()](function.ps-save.html) повинен супроводжуватись викликом **псrestore()**. Усі перетворення координат, налаштування стилю ліній, налаштування кольору тощо. відновлюються до стану до дзвінка [ps\_save()](function.ps-save.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_save()](function.ps-save.html) - Зберігає поточний контекст