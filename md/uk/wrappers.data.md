---
navigation:
  - wrappers.compression.md: '« zlib://'
  - wrappers.glob.md: 'glob:// »'
  - index.md: PHP Manual
  - wrappers.md: Підтримувані протоколи та обгортки
title: 'data://'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# data://

data:// - Схема Data (RFC 2397)

### Опис

data: ([» RFC 2397](http://www.faqs.org/rfcs/rfc2397)) - це обгортка потоків.

### Використання

-   data://text/plain;base64,

### Опції

**Основна інформація**

| Атрибут | Поддержка |
| --- | --- |
| Обмеження по [allow\_url\_fopen](filesystem.configuration.md#ini.allow-url-fopen) | Так |
| Обмеження по [allow\_url\_include](filesystem.configuration.md#ini.allow-url-include) | Так |
| Читання | Так |
| Запис | Ні |
| Додавання | Ні |
| Читання та запис одночасно | Ні |
| Поддержка[stat()](function.stat.md) | Ні |
| Поддержка[unlink()](function.unlink.md) | Ні |
| Поддержка[rename()](function.rename.md) | Ні |
| Поддержка[mkdir()](function.mkdir.md) | Ні |
| Поддержка[rmdir()](function.rmdir.md) | Ні |

### Приклади

**Приклад #1 Виведення вмісту data://**

```php
<?php
// выводит "I love PHP"
echo file_get_contents('data://text/plain;base64,SSBsb3ZlIFBIUAo=');
?>
```

**Приклад #2 Отримання типу потоку**

```php
<?php
$fp   = fopen('data://text/plain;base64,', 'r');
$meta = stream_get_meta_data($fp);

// выводит "text/plain"
echo $meta['mediatype'];
?>
```
