---
navigation:
  - splfileinfo.openfile.md: '« SplFileInfo::openFile'
  - splfileinfo.setinfoclass.md: 'SplFileInfo::setInfoClass »'
  - index.md: PHP Manual
  - class.splfileinfo.md: SplFileInfo
title: 'SplFileInfo::setFileClass'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileInfo::setFileClass

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplFileInfo::setFileClass — Задає ім'я класу, який використовуватиметься методом [SplFileInfo::openFile()](splfileinfo.openfile.md)

### Опис

```methodsynopsis
public SplFileInfo::setFileClass(string $class = SplFileObject::class): void
```

Задає ім'я класу, яке використовуватиме метод [SplFileInfo::openFile()](splfileinfo.openfile.md). Цим класом має бути [SplFileObject](class.splfileobject.md)или наследник класса[SplFileObject](class.splfileobject.md)

### Список параметрів

`class`

Имя класса для метода[SplFileInfo::openFile()](splfileinfo.openfile.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**SplFileInfo::setFileClass()\*\*\*\*

```php
<?php
// Создать класс, расширяющий SplFileObject
class MyFoo extends SplFileObject {}

$info = new SplFileInfo(__FILE__);
// Установить имя класса для использования
$info->setFileClass('MyFoo');
var_dump($info->openFile());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(MyFoo)#2 (0) { }
```

### Дивіться також

-   [SplFileInfo::openFile()](splfileinfo.openfile.md) \- Отримує об'єкт SplFileObject для файлу
