Отримує час останньої зміни

-   [« SplFileInfo::getLinkTarget](splfileinfo.getlinktarget.html)
    
-   [SplFileInfo::getOwner »](splfileinfo.getowner.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує час останньої зміни
    

# SplFileInfo::getMTime

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getMTime — Отримує час останньої зміни

### Опис

```methodsynopsis
public SplFileInfo::getMTime(): int|false
```

Повертає час, коли вміст файлу було змінено. Час повертається у форматі тимчасової мітки Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останньої зміни файлу у форматі тимчасової мітки Unix у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [filemtime()](function.filemtime.html) - Повертає час останньої зміни файлу