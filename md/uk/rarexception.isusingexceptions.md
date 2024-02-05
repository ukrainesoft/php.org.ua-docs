---
navigation:
  - class.rarexception.md: « RarException
  - rarexception.setusingexceptions.md: 'RarException::setUsingExceptions »'
  - index.md: PHP Manual
  - class.rarexception.md: RarException
title: 'RarException::isUsingExceptions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**RarException::isUsingExceptions()\*\*\*\*

```php
<?php
//По умолчанию исключения не используются
var_dump(RarException::isUsingExceptions());
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
```

### Дивіться також

-   [RarException::setUsingExceptions()](rarexception.setusingexceptions.md) \- Включити або вимкнути генерацію винятків замість повернення помилок
