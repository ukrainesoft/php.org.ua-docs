---
navigation:
  - splfileinfo.getrealpath.md: '« SplFileInfo::getRealPath'
  - splfileinfo.gettype.md: 'SplFileInfo::getType »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getSize

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getSize — Отримує розмір файлу

### Опис

```methodsynopsis
public SplFileInfo::getSize(): int|false
```

Повертає розмір файлу у байтах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Розмір файлу в байтах у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Буде викинуто виняток [RuntimeException](class.runtimeexception.md)якщо файл не існує або виникла помилка.

### Приклади

**Пример #1 Пример использования**SplFileInfo::getSize()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.jpg');
echo $fileinfo->getFilename() . " " . $fileinfo->getSize();
?>
```

Висновок наведеного прикладу буде схожим на:

```
example.jpg 15385
```

### Дивіться також

-   [filesize()](function.filesize.md) \- Повертає розмір файлу
