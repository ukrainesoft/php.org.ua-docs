---
navigation:
  - splfileinfo.getlinktarget.md: '« SplFileInfo::getLinkTarget'
  - splfileinfo.getowner.md: 'SplFileInfo::getOwner »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getMTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getMTime

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getMTime — Отримує час останньої зміни

### Опис

```methodsynopsis
public SplFileInfo::getMTime(): int|false
```

Повертає час, коли вміст файлу було змінено. Час повертається у форматі тимчасової мітки Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останньої зміни файлу у форматі тимчасової мітки Unix у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SplFileInfo::getMTime()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.jpg');
echo 'Последнее изменение в ' . date('g:i a', $info->getMTime());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Последнее изменение в 1:49 pm
```

### Дивіться також

-   [filemtime()](function.filemtime.md) \- Повертає час останньої зміни файлу
-   [SplFileInfo::getATime()](splfileinfo.getatime.md) \- Отримує час останнього доступу до файлу
-   [SplFileInfo::getCTime()](splfileinfo.getctime.md) \- Повертає час останньої зміни індексного дескриптора файлу
