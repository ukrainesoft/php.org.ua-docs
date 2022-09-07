---
navigation:
  - phar.setdefaultstub.md: '« Phar::setDefaultStub'
  - phar.setsignaturealgorithm.md: 'Phar::setSignatureAlgorithm »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::setMetadata'
---
# Phar::setMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::setMetadata — Встановити метадані phar-архіву

### Опис

```methodsynopsis
public Phar::setMetadata(mixed $metadata): void
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Функція **Phar::setMetadata()** використовується для збереження даних, що характеризують phar-архів загалом . [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.md) використовується для встановлення метаданих для файлу. Якщо метаданих буде багато, це може знизити швидкість завантаження phar-архіву.

Метадані можна використовувати, наприклад, для вказівки, який файл повинен виконуватися під час завантаження, або для вказівки розташування маніфесту, типу package.xml для модуля [» PEAR](https://pear.php.net/). Загалом будь-які корисні в контексті phar-архіву дані.

### Список параметрів

`metadata`

Будь-яка змінна PHP, що містить необхідну інформацію

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **Phar::setMetadata()****

```php
<?php
// удалим, на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.php'] = '<?php echo "привет"';
    $p->setMetadata(array('bootstrap' => 'file.php'));
    var_dump($p->getMetadata());
} catch (Exception $e) {
    echo 'Не могу создать/изменить phar:', $e;
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

-   [Phar::getMetadata()](phar.getmetadata.md) - Витягти метадані phar-архіву
-   [Phar::delMetadata()](phar.delmetadata.md) - Видалити глобальні метадані в архіві phar
-   [Phar::hasMetadata()](phar.hasmetadata.md) - Перевірити, чи містить phar-архів глобальні метадані
