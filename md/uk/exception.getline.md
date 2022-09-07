---
navigation:
  - exception.getfile.md: '« Exception::getFile'
  - exception.gettrace.md: 'Exception::getTrace »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getLine'
---
# Exception::getLine

(PHP 5, PHP 7, PHP 8)

Exception::getLine — Отримує рядок, у якому виник виняток

### Опис

```methodsynopsis
final public Exception::getLine(): int
```

Отримати номер рядка, де виняток було створено

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає номер рядка, де було створено виняток.

### Приклади

**Приклад #1 Приклад використання **Exception::getLine()****

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке");
} catch(Exception $e) {
    echo "Исключение было создано на строке: " . $e->getLine();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Исключение было создано на строке: 3
```

### Дивіться також

-   [Throwable::getLine()](throwable.getline.md) - Отримує рядок скрипта, в якому цей об'єкт був викинутий
