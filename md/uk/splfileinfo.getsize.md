---
navigation:
  - splfileinfo.getrealpath.html: '« SplFileInfo::getRealPath'
  - splfileinfo.gettype.html: 'SplFileInfo::getType »'
  - index.html: PHP Manual
  - class.splfileinfo.html: SplFileInfo
title: 'SplFileInfo::getSize'
---
# SplFileInfo::getSize

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getSize — Отримує розмір файлу

### Опис

```methodsynopsis
public SplFileInfo::getSize(): int|false
```

Повертає розмір файлу у байтах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Розмір файлу в байтах у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Буде викинуто виняток [RuntimeException](class.runtimeexception.html)якщо файл не існує або виникла помилка.

### Дивіться також

-   [filesize()](function.filesize.html) - Повертає розмір файлу
