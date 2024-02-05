---
navigation:
  - error.getprevious.md: '« Error::getPrevious'
  - error.getfile.md: 'Error::getFile »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::getCode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::getCode

(PHP 7, PHP 8)

Error::getCode — Повертає код помилки

### Опис

```methodsynopsis
final public Error::getCode(): int
```

Повертає код помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код помилки типу int

### Приклади

**Приклад #1 Приклад використання**Error::getCode()\*\*\*\*

```php
<?php
try {
    throw new Error("Какое-то сообщение об ошибке", 30);
} catch(Error $e) {
    echo "Код ошибки: " . $e->getCode();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Код ошибки: 30
```

### Дивіться також

-   [Throwable::getCode()](throwable.getcode.md) \- Повертає код виключення
