---
navigation:
  - phar.getalias.md: '« Phar::getAlias'
  - phar.getmodified.md: 'Phar::getModified »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::getMetadata'
---
# Phar::getMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::getMetadata — Витягти метадані phar-архіву

### Опис

```methodsynopsis
public Phar::getMetadata(array $unserializeOptions = []): mixed
```

Повертає метадані phar-архіву. Метаданими може бути будь-яка змінна PHP, яка може бути серіалізована.

### Список параметрів

Без параметрів.

### Значення, що повертаються

Будь-яке значення PHP, яке може бути серіалізоване та зберігається як метадані для архіву Phar, або \*\*`null`\*\*якщо метадані відсутні.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `unserializeOptions` |

### Приклади

**Приклад #1 Приклад використання **Phar::getMetadata()****

```php
<?php
// Убедимся, что архив не существует
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.php'] = '<?php echo "hello";';
    $p->setMetadata(array('bootstrap' => 'file.php'));
    var_dump($p->getMetadata());
} catch (Exception $e) {
    echo 'Не удалось изменить phar:', $e;
}
?>
```

Результат виконання цього прикладу:

```
array(1) {
  ["bootstrap"]=>
  string(8) "file.php"
}
```

### Дивіться також

-   [Phar::setMetadata()](phar.setmetadata.md) - Встановити метадані phar-архіву
-   [Phar::delMetadata()](phar.delmetadata.md) - Видалити глобальні метадані в архіві phar
-   [Phar::hasMetadata()](phar.hasmetadata.md) - Перевірити, чи містить phar-архів глобальні метадані
