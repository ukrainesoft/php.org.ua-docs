---
navigation:
  - splfileinfo.getbasename.md: '« SplFileInfo::getBasename'
  - splfileinfo.getextension.md: 'SplFileInfo::getExtension »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getCTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getCTime

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getCTime — Повертає час останньої зміни індексного дескриптора файлу

### Опис

```methodsynopsis
public SplFileInfo::getCTime(): int|false
```

Повертає час останньої зміни індексного дескриптора файлу. Повертає тимчасову мітку Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Час останньої зміни у вигляді тимчасової мітки Unix у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі виникнення помилки викидає виняток [RunTimeException](class.runtimeexception.md)

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getCTime()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.jpg');
echo 'Время последнего изменения ' . date('g:i a', $info->getCTime());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Время последнего изменения 1:49 pm
```

### Дивіться також

-   [filectime()](function.filectime.md) \- Повертає час зміни індексного дескриптора файлу
-   [SplFileInfo::getATime()](splfileinfo.getatime.md) \- Отримує час останнього доступу до файлу
-   [SplFileInfo::getMTime()](splfileinfo.getmtime.md) \- Отримує час останньої зміни
