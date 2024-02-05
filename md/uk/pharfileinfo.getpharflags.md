---
navigation:
  - pharfileinfo.getmetadata.md: '« PharFileInfo::getMetadata'
  - pharfileinfo.hasmetadata.md: 'PharFileInfo::hasMetadata »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::getPharFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharFileInfo::getPharFlags

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::getPharFlags — Отримати прапори файлу в phar-архіві

### Опис

```methodsynopsis
public PharFileInfo::getPharFlags(): int
```

Повертає набір прапорів, заданих у маніфесті Phar-архіву. У поточній реалізації завжди повертає

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Флаги Phar-архива (пока всегда ) .

### Приклади

**Пример #1 Пример использования**PharFileInfo::getPharFlags()\*\*\*\*

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->getPharFlags());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить my.phar: ', $e;
}
?>
```

Результат виконання наведеного прикладу:

```
int(0)
```
