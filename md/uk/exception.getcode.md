---
navigation:
  - exception.getprevious.md: '« Exception::getPrevious'
  - exception.getfile.md: 'Exception::getFile »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getCode'
---
# Exception::getCode

(PHP 5, PHP 7, PHP 8)

Exception::getCode — Отримує код виключення

### Опис

```methodsynopsis
final public Exception::getCode(): int
```

Повертає код виключення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає код виключення типу int у класу [Exception](class.exception.md), але у нащадків класу [Exception](class.exception.md) може бути інший тип (наприклад, типу string в [PDOException](class.pdoexception.md)

### Приклади

**Приклад #1 Приклад використання **Exception::getCode()****

```php
<?php
try {
    throw new Exception("Какое-нибудь сообщение об ошибке", 30);
} catch(Exception $e) {
    echo "Код исключения: " . $e->getCode();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Код исключения: 30
```

### Дивіться також

-   [Throwable::getCode()](throwable.getcode.md) - Повертає код виключення
