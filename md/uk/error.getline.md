---
navigation:
  - error.getfile.html: '« Error::getFile'
  - error.gettrace.html: 'Error::getTrace »'
  - index.html: PHP Manual
  - class.error.html: Error
title: 'Error::getLine'
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
try {
    throw new Error("Какое-то сообщение об ошибке");
} catch(Error $e) {
    echo "Ошибка создана в строке: " . $e->getLine();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ошибка создана в строке: 3
```

### Дивіться також

-   [Throwable::getLine()](throwable.getline.html) - Отримує рядок скрипта, в якому цей об'єкт було викинуто
