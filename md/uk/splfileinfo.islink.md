---
navigation:
  - splfileinfo.isfile.md: '« SplFileInfo::isFile'
  - splfileinfo.isreadable.md: 'SplFileInfo::isReadable »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::isLink'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::isLink

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::isLink — Вказує, чи є файл посиланням

### Опис

```methodsynopsis
public SplFileInfo::isLink(): bool
```

Використовуйте цей метод, щоб перевірити, чи є файл, на який посилається об'єкт SplFileInfo, посиланням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл є посиланням; **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**SplFileInfo::isLink()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/path/to/symlink');
if ($info->isLink()) {
    echo 'Реальный путь: '.$info->getRealPath();
}
?>
```

### Дивіться також

-   [SplFileInfo::getRealPath()](splfileinfo.getrealpath.md) \- Отримує абсолютний шлях до файлу
