---
navigation:
  - error.gettraceasstring.md: '« Error::getTraceAsString'
  - error.clone.md: 'Error::\_\_clone »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::\_\_function toString() { \[native code\] }

(PHP 7, PHP 8)

Error::\_\_toString — Строкове подання помилки

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

**Приклад #1 Приклад використання** Error::\_\_toString()\*\*\*\*

```php
<?php
try {
    throw new Error("Сообщение об ошибке");
} catch(Error $e) {
    echo $e;
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Error: Сообщение об ошибке in /home/bjori/tmp/ex.php:3
Stack trace:
#0 {main}
```

### Дивіться також

-   [Throwable::\_\_toString()](throwable.tostring.md) \- отримує рядкове подання викинутого об'єкта
