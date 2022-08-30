Скомпілювати та закешувати, але не виконувати скрипт PHP

-   [« Функции OPcache](ref.opcache.md)
    
-   [opcachegetconfiguration »](function.opcache-get-configuration.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OPcache](ref.opcache.md)
    
-   Скомпілювати та закешувати, але не виконувати скрипт PHP
    

# opcachecompilefile

(PHP 5> = 5.5.5, PHP 7, PHP 8, PECL ZendOpcache > 7.0.2)

opcachecompilefile — Скомпілювати та закешувати, але не виконувати скрипт PHP

### Опис

```methodsynopsis
opcache_compile_file(string $filename): bool
```

Ця функція компілює PHP-скрипт і поміщає його в кеш опкодів, але не запускає його. Ви можете використовувати для прогрівання кеша після перезапуску веб-сервера.

### Список параметрів

`filename`

Шлях до скрипту PHP.

### Значення, що повертаються

Повертає **`true`**, якщо `filename` успішно скомпільований або **`false`** у разі виникнення помилки.

### Помилки

Якщо `filename` не може бути завантажений або скомпільований, буде видана помилка рівня **`E_WARNING`**. Для придушення попередження можна використовувати[](language.operators.errorcontrol.md)

### Дивіться також

-   [opcacheinvalidate()](function.opcache-invalidate.html) - анулює закешований скрипт