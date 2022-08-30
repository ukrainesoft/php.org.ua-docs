Визначає MIME-тип вмісту файлу

-   [« finfosetflags](function.finfo-set-flags.html)
    
-   [finfo »](class.finfo.md)
    
-   [PHP Manual](index.md)
    
-   [Функции модуля Fileinfo](ref.fileinfo.md)
    
-   Визначає MIME-тип вмісту файлу
    

# mimecontenttype

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

mimecontenttype — Визначає тип MIME вмісту файлу.

### Опис

```methodsynopsis
mime_content_type(resource|string $filename): string|false
```

Повертає MIME-тип вмісту файлу, використовуючи визначення інформації з файла magic.mime.

### Список параметрів

`filename`

Шлях до файлу, що перевіряється.

### Значення, що повертаються

Повертає тип вмісту у форматі MIME, наприклад `text/plain` або `application/octet-stream` або **`false`** у разі виникнення помилки.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад **mimecontenttype()****

```php
<?php
echo mime_content_type('php.gif') . "\n";
echo mime_content_type('test.php');
?>
```

Результат виконання цього прикладу:

```
image/gif
text/plain
```

### Дивіться також

-   [finfofile()](finfo.file.md) - Псевдонім finfofile()
-   [finfobuffer()](finfo.buffer.md) - Псевдонім finfobuffer()