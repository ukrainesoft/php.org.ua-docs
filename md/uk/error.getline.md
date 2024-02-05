---
navigation:
  - error.getfile.md: '« Error::getFile'
  - error.gettrace.md: 'Error::getTrace »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::getLine'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::getLine

(PHP 7, PHP 8)

Error::getLine — Отримує номер рядка, в якому сталася помилка

### Опис

```methodsynopsis
final public Error::getLine(): int
```

Отримати номер рядка, в якому сталася помилка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер рядка, в якому сталася помилка.

### Приклади

**Приклад #1 Приклад використання**Error::getLine()\*\*\*\*

```php
<?php
try {
    throw new Error("Какое-то сообщение об ошибке");
} catch(Error $e) {
    echo "Ошибка создана в строке: " . $e->getLine();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ошибка создана в строке: 3
```

### Дивіться також

-   [Throwable::getLine()](throwable.getline.md) \- Отримує рядок скрипта, в якому цей об'єкт був викинутий
