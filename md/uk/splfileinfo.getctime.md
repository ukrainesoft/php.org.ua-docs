---
navigation:
  - splfileinfo.getbasename.md: '« SplFileInfo::getBasename'
  - splfileinfo.getextension.md: 'SplFileInfo::getExtension »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getCTime'
---
# SplFileInfo::getCTime

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::getCTime — Повертає час останньої зміни індексного дескриптора файлу

### Опис

```methodsynopsis
public SplFileInfo::getCTime(): int|false
```

Повертає час останньої зміни індексного дескриптора файлу. Повертає тимчасову мітку Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Час останньої зміни у вигляді тимчасової мітки Unix у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

У разі виникнення помилки викидає виняток [RunTimeException](class.runtimeexception.md)

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::getCTime()****

```php
<?php
$info = new SplFileInfo(__FILE__);
echo 'Время последнего изменения ' . date('g:i a', $info->getCTime());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Время последнего изменения 1:49 pm
```

### Дивіться також

-   [filectime()](function.filectime.md) - Повертає час зміни індексного дескриптора файлу
