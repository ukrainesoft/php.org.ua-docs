---
navigation:
  - splfileinfo.islink.md: '« SplFileInfo::isLink'
  - splfileinfo.iswritable.md: 'SplFileInfo::isWritable »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::isReadable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::isReadable

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::isReadable — Вказує, чи є файл доступним для читання

### Опис

```methodsynopsis
public SplFileInfo::isReadable(): bool
```

Перевіряє, чи файл доступний для читання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл доступний для читання; **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**SplFileInfo::isReadable()\*\*\*\*

```php
<?php
$info = new SplFileInfo('readable.jpg');
if ($info->isReadable()) {
    echo $info->getFilename() . ' доступен для чтения';
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
readable.jpg доступен для чтения
```
