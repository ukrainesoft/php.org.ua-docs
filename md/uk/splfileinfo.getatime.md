Отримує час останнього доступу до файлу

-   [« SplFileInfo::\_\_construct](splfileinfo.construct.html)
    
-   [SplFileInfo::getBasename »](splfileinfo.getbasename.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileInfo](class.splfileinfo.html)
    
-   Отримує час останнього доступу до файлу
    

# SplFileInfo::getATime

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getATime — Отримує час останнього доступу до файлу

### Опис

```methodsynopsis
public SplFileInfo::getATime(): int|false
```

Отримує час останнього доступу до файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останнього звернення до файлу у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Викидає [RunTimeException](class.runtimeexception.html) у разі виникнення помилки.

### Дивіться також

-   [fileatime()](function.fileatime.html) - Повертає час останнього доступу до файлу