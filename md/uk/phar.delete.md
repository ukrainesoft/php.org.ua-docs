---
navigation:
  - phar.delmetadata.md: '« Phar::delMetadata'
  - phar.destruct.md: 'Phar::\_\_destruct »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::delete

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::delete — Видалення файлу всередині phar-архіву

### Опис

```methodsynopsis
public Phar::delete(string $localName): bool
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Видаляє файл із архіву. Ця функція аналогічна виклику [unlink()](function.unlink.md) для обгортки потоку, як показано в прикладі нижче.

### Список параметрів

`localName`

Шлях всередині архіву для видалення файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, але краще перевірити, чи було викинуто виняток, і вважати успішним виклик, у результаті якого викинуто виняток.

### Помилки

Викидає виняток [PharException](class.pharexception.md), якщо виникли помилки під час запису змін на диск.

### Приклади

**Пример #1 Пример использования**Phar::delete()\*\*\*\*

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->delete('удали/меня.php');
    // это эквивалентно следующему:
    unlink('phar://myphar.phar/удали/меня.php');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [PharData::delete()](phardata.delete.md) \- Видалити файл із tar/zip-архіву
-   [Phar::unlinkArchive()](phar.unlinkarchive.md) \- Повністю видалити архів з пам'яті та з диска
