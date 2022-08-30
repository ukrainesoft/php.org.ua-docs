Перевіряє, чи закешовано скрипт в OPCache

-   [« opcacheinvalidate](function.opcache-invalidate.html)
    
-   [opcachereset »](function.opcache-reset.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OPcache](ref.opcache.md)
    
-   Перевіряє, чи закешовано скрипт в OPCache
    

# opcacheісscriptcached

(PHP 5> = 5.5.11, PHP 7, PHP 8, PECL ZendOpcache> = 7.0.4)

opcacheісscriptcached — Перевіряє, чи закешовано скрипт в OPCache

### Опис

```methodsynopsis
opcache_is_script_cached(string $filename): bool
```

Функція перевіряє, чи вказаний скрипт в OPCache. Може бути використана для визначення прогріти кеш для конкретного скрипту. Функція перевіряє лише кеш у пам'яті, не перевіряючи файловий кеш.

### Список параметрів

`filename`

Шлях до файлу сценарію.

### Значення, що повертаються

Повертає **`true`**, якщо `filename` закешований в OPCache, **`false`** якщо ні.

### Дивіться також

-   [opcachecompilefile()](function.opcache-compile-file.html) - Скомпілювати та закешувати, але не виконувати скрипт PHP