---
navigation:
  - splfileobject.current.md: '« SplFileObject::current'
  - splfileobject.fflush.md: 'SplFileObject::fflush »'
  - index.md: PHP Manual
  - class.splfileobject.md: SplFileObject
title: 'SplFileObject::eof'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFileObject::eof

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplFileObject::eof — Перевіряє, чи кінець файлу досягнуто.

### Опис

```methodsynopsis
public SplFileObject::eof(): bool
```

Визначає, чи було досягнуто кінця файлу

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо кінець файлу було досягнуто; **`false`** в іншому випадку.

### Приклади

**Пример #1 Пример использования**SplFileObject::eof()\*\*\*\*

```php
<?php
$file = new SplFileObject("fruits.txt");
while ( ! $file->eof()) {
    echo $file->fgets();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
apple
banana
cherry
date
elderberry
```

### Дивіться також

-   [SplFileObject::valid()](splfileobject.valid.md) \- Перевіряє, чи кінець файлу (EOF) досягнуто.
-   [feof()](function.feof.md) \- Перевіряє, чи кінець файлу досягнуто
