---
navigation:
  - splfileobject.getcurrentline.html: '« SplFileObject::getCurrentLine'
  - splfileobject.getmaxlinelen.html: 'SplFileObject::getMaxLineLen »'
  - index.html: PHP Manual
  - class.splfileobject.html: SplFileObject
title: 'SplFileObject::getFlags'
---
# SplFileObject::getFlags

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::getFlags — Отримує прапори налаштування об'єкта SplFileObject

### Опис

```methodsynopsis
public SplFileObject::getFlags(): int
```

Отримує прапори налаштування об'єкта SplFileObject як цілого числа типу int.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає число типу int, яке представляє набір прапорів.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::getFlags()****

```php
<?php
$file = new SplFileObject(__FILE__, "r");

if ($file->getFlags() & SplFileObject::SKIP_EMPTY) {
    echo "Пропускать пустые строки\n";
} else {
    echo "Не пропускать пустые строки\n";
}

$file->setFlags(SplFileObject::SKIP_EMPTY);

if ($file->getFlags() & SplFileObject::SKIP_EMPTY) {
    echo "Пропускать пустые строки\n";
} else {
    echo "Не пропускать пустые строки\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Не пропускать пустые строки
Пропускать пустые строки
```

### Дивіться також

-   [SplFileObject::setFlags()](splfileobject.setflags.html) - Встановлює прапори для SplFileObject
