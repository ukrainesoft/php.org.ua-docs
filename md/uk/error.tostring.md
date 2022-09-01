---
navigation:
  - error.gettraceasstring.md: '« Error::getTraceAsString'
  - error.clone.md: 'Error::clone »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::function toString() { \[native code\] }'
---
# Error::function toString() { \[native code\] }

(PHP 7, PHP 8)

Error::toString — Строкове подання помилки

### Опис

```methodsynopsis
public Error::__toString(): string
```

Повертає рядкове (string) уявлення помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядкове (string) уявлення помилки.

### Приклади

**Приклад #1 Приклад використання **Error::toString()****

```php
<?php
try {
    throw new Error("Сообщение об ошибке");
} catch(Error $e) {
    echo $e;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Error: Сообщение об ошибке in /home/bjori/tmp/ex.php:3
Stack trace:
#0 {main}
```

### Дивіться також

-   [Throwable::toString()](throwable.tostring.md) - отримує рядкове подання викинутого об'єкта
