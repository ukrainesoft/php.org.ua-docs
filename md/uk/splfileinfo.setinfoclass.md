---
navigation:
  - splfileinfo.setfileclass.md: '« SplFileInfo::setFileClass'
  - splfileinfo.tostring.md: 'SplFileInfo::toString »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::setInfoClass'
---
# SplFileInfo::setInfoClass

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::setInfoClass — Задає ім'я класу, об'єкти якого створюватимуться методами [SplFileInfo::getFileInfo()](splfileinfo.getfileinfo.md) і [SplFileInfo::getPathInfo()](splfileinfo.getpathinfo.md)

### Опис

```methodsynopsis
public SplFileInfo::setInfoClass(string $class = SplFileInfo::class): void
```

Задає ім'я класу, об'єкти якого створюватимуться під час виклику методів [SplFileInfo::getFileInfo()](splfileinfo.getfileinfo.md) і [SplFileInfo::getPathInfo()](splfileinfo.getpathinfo.md). Клас має бути [SplFileInfo](class.splfileinfo.md) або класом, похідним від [SplFileInfo](class.splfileinfo.md)

### Список параметрів

`class`

Ім'я класу, який використовуватиметься під час виклику [SplFileInfo::getFileInfo()](splfileinfo.getfileinfo.md) і [SplFileInfo::getPathInfo()](splfileinfo.getpathinfo.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання [SplFileInfo::setFileClass()](splfileinfo.setfileclass.md)**

```php
<?php
// Определить класс, который расширяет SplFileInfo
class MyFoo extends SplFileInfo {}

$info = new SplFileInfo('foo');
// Установить имя класса для использования
$info->setInfoClass('MyFoo');
var_dump($info->getFileInfo());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MyFoo)#2 (0) { }
```

### Дивіться також

-   [SplFileInfo::getFileInfo()](splfileinfo.getfileinfo.md) - Отримує об'єкт SplFileInfo для файлу
