---
navigation:
  - exception.getcode.md: '« Exception::getCode'
  - exception.getline.md: 'Exception::getLine »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::getFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception::getFile

(PHP 5, PHP 7, PHP 8)

Exception::getFile — Отримує файл, у якому виник виняток

### Опис

```methodsynopsis
final public Exception::getFile(): string
```

Отримати ім'я файлу, де виняток було створено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, в якому виняток створено.

### Приклади

**Приклад #1 Приклад використання** Exception::getFile()\*\*\*\*

```php
<?php
try {
    throw new Exception;
} catch(Exception $e) {
    echo $e->getFile();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
/home/bjori/tmp/ex.php
```

### Дивіться також

-   [Throwable::getFile()](throwable.getfile.md) \- Повертає файл, у якому викинуто виняток
