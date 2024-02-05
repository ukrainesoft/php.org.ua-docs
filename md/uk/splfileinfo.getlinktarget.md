---
navigation:
  - splfileinfo.getinode.md: '« SplFileInfo::getInode'
  - splfileinfo.getmtime.md: 'SplFileInfo::getMTime »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::getLinkTarget'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::getLinkTarget

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

SplFileInfo::getLinkTarget — Отримує шлях посилання

### Опис

```methodsynopsis
public SplFileInfo::getLinkTarget(): string|false
```

Отримує цільовий шлях посилання файлової системи.

> **Зауваження** :
> 
> Цей шлях може бути реальним розташуванням у файлової системі. Щоб отримати реальний шлях файлової системи, використовуйте метод [SplFileInfo::getRealPath()](splfileinfo.getrealpath.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає цільовий шлях посилання файлової системи у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

У разі виникнення помилки викидає виняток [RuntimeException](class.runtimeexception.md)

### Приклади

**Пример #1 Пример использования**SplFileInfo::getLinkTarget()\*\*\*\*

```php
<?php
$info = new SplFileInfo('/Users/bbieber/workspace');
if ($info->isLink()) {
    var_dump($info->getLinkTarget());
    var_dump($info->getRealPath());
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(19) "Documents/workspace"
string(34) "/Users/bbieber/Documents/workspace"
```

### Дивіться також

-   [SplFileInfo::isLink()](splfileinfo.islink.md) \- Вказує, чи є файл посиланням
-   [SplFileInfo::getRealPath()](splfileinfo.getrealpath.md) \- Отримує абсолютний шлях до файлу
