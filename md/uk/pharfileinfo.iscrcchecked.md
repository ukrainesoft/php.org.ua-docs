---
navigation:
  - pharfileinfo.hasmetadata.md: '« PharFileInfo::hasMetadata'
  - pharfileinfo.iscompressed.md: 'PharFileInfo::isCompressed »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::isCRCChecked'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharFileInfo::isCRCChecked

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::isCRCChecked — Визначити, чи пройшов файл перевірку CRC

### Опис

```methodsynopsis
public PharFileInfo::isCRCChecked(): bool
```

Визначає, чи файл пройшов перевірку CRC.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**, якщо файл пройшов перевірку CRC, **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**PharFileInfo::isCRCChecked()\*\*\*\*

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->isCRCChecked());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить my.phar: ', $e;
}
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
