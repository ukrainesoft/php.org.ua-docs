---
navigation:
  - splfileinfo.getctime.md: '« SplFileInfo::getCTime'
  - splfileinfo.getfileinfo.md: 'SplFileInfo::getFileInfo »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getExtension'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getExtension

(PHP 5 >= 5.3.6, PHP 7, PHP 8)

SplFileInfo::getExtension — Отримує розширення файлу

### Опис

```methodsynopsis
public SplFileInfo::getExtension(): string
```

Повертає розширення файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), що містить розширення файлу, або порожній рядок (string), якщо файл не має розширення.

### Приклади

**Пример #1 Пример использования**SplFileInfo::getExtension()\*\*\*\*

```php
<?php

$info = new SplFileInfo('foo.txt');
var_dump($info->getExtension());

$info = new SplFileInfo('photo.jpg');
var_dump($info->getExtension());

$info = new SplFileInfo('something.tar.gz');
var_dump($info->getExtension());

?>
```

Результат виконання наведеного прикладу:

```
string(3) "txt"
string(3) "jpg"
string(2) "gz"
```

### Примітки

> **Зауваження** :
> 
> Другой способ для получения расширения - использование функции[pathinfo()](function.pathinfo.md)
> 
> ```php
> <?php
> $extension = pathinfo($info->getFilename(), PATHINFO_EXTENSION);
> ?>
> ```

### Дивіться також

-   [SplFileInfo::getFilename()](splfileinfo.getfilename.md) \- Отримує ім'я файлу
-   [SplFileInfo::getBasename()](splfileinfo.getbasename.md) \- Отримує базове ім'я файлу
-   [pathinfo()](function.pathinfo.md) \- Повертає інформацію про шлях до файлу
