---
navigation:
  - splfileinfo.construct.md: '« SplFileInfo::\_\_construct'
  - splfileinfo.getbasename.md: 'SplFileInfo::getBasename »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getATime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getATime

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getATime — Отримує час останнього доступу до файлу

### Опис

```methodsynopsis
public SplFileInfo::getATime(): int|false
```

Отримує час останнього доступу до файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час останнього звернення до файлу у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викидає [RunTimeException](class.runtimeexception.md)в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getATime()\*\*\*\*

```php
<?php
$info = new SplFileInfo('example.jpg');
echo 'Последнего обращения к файлу в ' . date('g:i a', $info->getATime());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Последнего обращения к файлу в 1:49 pm
```

### Дивіться також

-   [fileatime()](function.fileatime.md) \- Повертає час останнього доступу до файлу
