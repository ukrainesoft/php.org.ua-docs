---
navigation:
  - splfileinfo.openfile.html: '« SplFileInfo::openFile'
  - splfileinfo.setinfoclass.html: 'SplFileInfo::setInfoClass »'
  - index.html: PHP Manual
  - class.splfileinfo.html: SplFileInfo
title: 'SplFileInfo::setFileClass'
---
# SplFileInfo::setFileClass

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplFileInfo::setFileClass — Задає ім'я класу, який використовуватиметься методом [SplFileInfo::openFile()](splfileinfo.openfile.html)

### Опис

```methodsynopsis
public SplFileInfo::setFileClass(string $class = SplFileObject::class): void
```

Задає ім'я класу, яке використовуватиме метод [SplFileInfo::openFile()](splfileinfo.openfile.html). Цим класом має бути [SplFileObject](class.splfileobject.html) або спадкоємець класу [SplFileObject](class.splfileobject.html)

### Список параметрів

`class`

Ім'я класу для методу [SplFileInfo::openFile()](splfileinfo.openfile.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplFileInfo::setFileClass()****

```php
<?php
// Создать класс, расширяющий SplFileObject
class MyFoo extends SplFileObject {}

$info = new SplFileInfo(__FILE__);
// Установить имя класса для использования
$info->setFileClass('MyFoo');
var_dump($info->openFile());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(MyFoo)#2 (0) { }
```

### Дивіться також

-   [SplFileInfo::openFile()](splfileinfo.openfile.html) - Отримує об'єкт SplFileObject для файлу
