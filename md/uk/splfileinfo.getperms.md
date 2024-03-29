---
navigation:
  - splfileinfo.getpathname.md: '« SplFileInfo::getPathname'
  - splfileinfo.getrealpath.md: 'SplFileInfo::getRealPath »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getPerms'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getPerms

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::getPerms — Отримує список дозволів

### Опис

```methodsynopsis
public SplFileInfo::getPerms(): int|false
```

Отримує список дозволів файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає список дозволів для файлу у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SplFileInfo::getPerms()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/tmp');
echo substr(sprintf('%o', $info->getPerms()), -4);

$info = new SplFileInfo(__FILE__);
echo substr(sprintf('%o', $info->getPerms()), -4);
?>
```

Висновок наведеного прикладу буде схожим на:

```
1777
0644
```
