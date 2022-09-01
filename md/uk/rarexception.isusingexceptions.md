---
navigation:
  - class.rarexception.html: « RarException
  - rarexception.setusingexceptions.html: 'RarException::setUsingExceptions »'
  - index.html: PHP Manual
  - class.rarexception.html: RarException
title: 'RarException::isUsingExceptions'
---
# RarException::isUsingExceptions

(PECL rar >= 2.0.0)

RarException::isUsingExceptions — Перевірити, чи будуть функції повертати помилки або викидати винятки

### Опис

```methodsynopsis
public static RarException::isUsingExceptions(): bool
```

Перевіряє, чи будуть функції RAR викидати винятки або повертати помилки та викликати попередження в більшості випадків (не включаючи деякі програмні помилки на кшталт передачі аргументів некоректних типів).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо використовуються винятки та **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **RarException::isUsingExceptions()****

```php
<?php
//По умолчанию исключения не используются
var_dump(RarException::isUsingExceptions());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
```

### Дивіться також

-   [RarException::setUsingExceptions()](rarexception.setusingexceptions.html) - Включити або вимкнути генерацію винятків замість повернення помилок
