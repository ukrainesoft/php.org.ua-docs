PHP-архів

-   [« glob://](wrappers.glob.md)
    
-   [ssh2:// »](wrappers.ssh2.md)
    
-   [PHP Manual](index.md)
    
-   [Підтримувані протоколи та обгортки](wrappers.md)
    
-   PHP-архів
    

# phar://

phar:// - PHP-архів

### Опис

Обгортка потоку phar://. Дивіться розділ [Обёртка потока Phar](phar.using.stream.md) для детальнішого опису.

### Використання

-   phar://

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allowurlfopen](filesystem.configuration.html#ini.allow-url-fopen) | Ні |
| Обмеження по [allowurlinclude](filesystem.configuration.html#ini.allow-url-include) | Ні |
| Читання | Так |
| Запис | Так |
| Додавання | Ні |
| Одночасне читання та запис | Так |
| Підтримка [stat()](function.stat.md) | Так |
| Підтримка [unlink()](function.unlink.md) | Так |
| Підтримка [rename()](function.rename.md) | Так |
| Підтримка [mkdir()](function.mkdir.md) | Так |
| Підтримка [rmdir()](function.rmdir.md) | Так |

### Дивіться також

-   [Контекстні опції Phar](context.phar.md)