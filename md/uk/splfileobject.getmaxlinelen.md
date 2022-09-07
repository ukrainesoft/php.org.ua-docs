---
navigation:
  - splfileobject.getflags.md: '« SplFileObject::getFlags'
  - splfileobject.haschildren.md: 'SplFileObject::hasChildren »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::getMaxLineLen'
---
# SplFileObject::getMaxLineLen

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::getMaxLineLen — Отримати максимальну довжину рядка

### Опис

```methodsynopsis
public SplFileObject::getMaxLineLen(): int
```

Отримує максимальну довжину рядка, встановлену за допомогою [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає максимальну довжину рядка, якщо вона була встановлена ​​за допомогою [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.md), за замовчуванням `0`

### Приклади

**Приклад #1 Приклад використання **SplFileObject::getMaxLineLen()****

```php
<?php
$file = new SplFileObject("file.txt");
var_dump($file->getMaxLineLen());

$file->setMaxLineLen(20);
var_dump($file->getMaxLineLen());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
int(20)
```

### Дивіться також

-   [SplFileObject::setMaxLineLen()](splfileobject.setmaxlinelen.md) - Встановити максимальну довжину рядка
