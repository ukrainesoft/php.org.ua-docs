---
navigation:
  - splfileobject.getcurrentline.md: '« SplFileObject::getCurrentLine'
  - splfileobject.getmaxlinelen.md: 'SplFileObject::getMaxLineLen »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::getFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::getFlags

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

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

**Пример #1 Пример использования**SplFileObject::getFlags()\*\*\*\*

```php
<?php
$file = new SplFileObject(__FILE__, "r");

if ($file->getFlags() & SplFileObject::SKIP_EMPTY) {
    echo "Пропускать пустые строки\n";
} else {
    echo "Не пропускать пустые строки\n";
}

$file->setFlags(SplFileObject::SKIP_EMPTY);

if ($file->getFlags() & SplFileObject::SKIP_EMPTY) {
    echo "Пропускать пустые строки\n";
} else {
    echo "Не пропускать пустые строки\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Не пропускать пустые строки
Пропускать пустые строки
```

### Дивіться також

-   [SplFileObject::setFlags()](splfileobject.setflags.md) \- Встановлює прапори для SplFileObject
