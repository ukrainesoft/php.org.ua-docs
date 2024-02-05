---
navigation:
  - error.getcode.md: '« Error::getCode'
  - error.getline.md: 'Error::getLine »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::getFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::getFile

(PHP 7, PHP 8)

Error::getFile — Отримує файл, у якому сталася помилка

### Опис

```methodsynopsis
final public Error::getFile(): string
```

Отримати ім'я файлу, в якому виникла помилка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, в якому виникла помилка.

### Приклади

**Пример #1 Пример использования**Error::getFile()\*\*\*\*

```php
<?php
try {
    throw new Error;
} catch(Error $e) {
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
