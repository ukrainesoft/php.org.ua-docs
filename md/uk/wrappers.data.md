Схема Data (RFC 2397)

-   [« zlib://](wrappers.compression.html)
    
-   [glob:// »](wrappers.glob.html)
    
-   [PHP Manual](index.html)
    
-   [Поддерживаемые протоколы и обёртки](wrappers.html)
    
-   Схема Data (RFC 2397)
    

# data://

data:// - Схема Data (RFC 2397)

### Опис

data: ([» RFC 2397](http://www.faqs.org/rfcs/rfc2397)) - це обгортка потоків.

### Використання

-   data://text/plain;base64,

### Опції

**Основна інформація**

| Атрибут                                                                                 | Поддержка |
|-----------------------------------------------------------------------------------------|-----------|
| Обмеження по [allow\_url\_fopen](filesystem.configuration.html#ini.allow-url-fopen)     | Так       |
| Обмеження по [allow\_url\_include](filesystem.configuration.html#ini.allow-url-include) | Так       |
| Читання                                                                                 | Так       |
| Запис                                                                                   | Ні        |
| Додавання                                                                               | Ні        |
| Читання та запис одночасно                                                              | Ні        |
| Підтримка [stat()](function.stat.html)                                                  | Ні        |
| Підтримка [unlink()](function.unlink.html)                                              | Ні        |
| Підтримка [rename()](function.rename.html)                                              | Ні        |
| Підтримка [mkdir()](function.mkdir.html)                                                | Ні        |
| Підтримка [rmdir()](function.rmdir.html)                                                | Ні        |

### Приклади

**Приклад #1 Виведення вмісту data://**

```php
<?php
// выводит "I love PHP"
echo file_get_contents('data://text/plain;base64,SSBsb3ZlIFBIUAo=');
?>
```

**Приклад #2 Отримання типу потоку**

```php
<?php
$fp   = fopen('data://text/plain;base64,', 'r');
$meta = stream_get_meta_data($fp);

// выводит "text/plain"
echo $meta['mediatype'];
?>
```