---
navigation:
  - function.finfo-set-flags.md: « finfo\_set\_flags
  - class.finfo.md: finfo »
  - index.md: PHP Manual
  - ref.fileinfo.md: Функції модуля Fileinfo
title: mime\_content\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mime\_content\_type

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

mime\_content\_type — Визначає тип MIME вмісту файлу.

### Опис

```methodsynopsis
mime_content_type(resource|string $filename): string|false
```

Повертає MIME-тип вмісту файлу, використовуючи визначення інформації з файла magic.mime.

### Список параметрів

`filename`

Шлях до файлу, що перевіряється.

### Значення, що повертаються

Повертає тип вмісту у форматі MIME, наприклад `text/plain`или`application/octet-stream`или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі невдалого завершення роботи генерується помилка рівня **`E_WARNING`**

### Приклади

**Приклад #1 Приклад**mime\_content\_type()\*\*\*\*

```php
<?php
echo mime_content_type('php.gif') . "\n";
echo mime_content_type('test.php');
?>
```

Результат виконання наведеного прикладу:

```
image/gif
text/plain
```

### Дивіться також

-   [finfo\_file()](finfo.file.md) \- Псевдонім finfo\_file()
-   [finfo\_buffer()](finfo.buffer.md) \- Псевдонім finfo\_buffer()
