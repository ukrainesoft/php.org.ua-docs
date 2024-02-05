---
navigation:
  - splfileinfo.isreadable.md: '« SplFileInfo::isReadable'
  - splfileinfo.openfile.md: 'SplFileInfo::openFile »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::isWritable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::isWritable

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::isWritable — Вказує, чи є файл доступним для запису

### Опис

```methodsynopsis
public SplFileInfo::isWritable(): bool
```

Перевіряє, чи поточний файл доступний для запису.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, если файл доступен для записи;**`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**SplFileInfo::isWriteable()\*\*\*\*

```php
<?php
$info = new SplFileInfo('locked.jpg');
if (!$info->isWriteable()) {
    echo $info->getFilename() . ' не доступен для записи';
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
locked.jpg не доступен для записи
```
