---
navigation:
  - class.splfileinfo.md: « SplFileInfo
  - splfileinfo.getatime.md: 'SplFileInfo::getATime »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::\_\_construct

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::\_\_construct — Створити новий об'єкт SplFileInfo

### Опис

public**SplFileInfo::\_\_construct**(string`$filename`) .

Створює новий об'єкт SplFileInfo для вказаного імені файлу. Файл не обов'язково має існувати чи бути доступним для читання.

### Список параметрів

`filename`

Шлях до файлу.

### Приклади

**Пример #1 Пример использования**SplFileInfo::\_\_construct()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.php');
if ($info->isFile()) {
    echo $info->getRealPath();
}
?>
```
