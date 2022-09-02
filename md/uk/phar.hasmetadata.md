---
navigation:
  - phar.getversion.md: '« Phar::getVersion'
  - phar.interceptfilefuncs.md: 'Phar::interceptFileFuncs »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::hasMetadata'
---
# Phar::hasMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

Phar::hasMetadata — Перевірити, чи містить phar-архів глобальні метадані

### Опис

```methodsynopsis
public Phar::hasMetadata(): bool
```

Перевіряє, чи містить phar-архів глобальні метадані.

### Список параметрів

Без параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`**

### Приклади

**Приклад #1 Приклад використання **Phar::hasMetadata()****

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    var_dump($phar->hasMetadata());
    $phar->setMetadata(array('thing' => 'hi'));
    var_dump($phar->hasMetadata());
    $phar->delMetadata();
    var_dump($phar->hasMetadata());
} catch (Exception $e) {
    // handle error
}
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [Phar::getMetadata()](phar.getmetadata.md) - Витягти метадані phar-архіву
-   [Phar::setMetadata()](phar.setmetadata.md) - Встановити метадані phar-архіву
-   [Phar::delMetadata()](phar.delmetadata.md) - Видалити глобальні метадані в архіві phar
