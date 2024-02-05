---
navigation:
  - pharfileinfo.iscompressed.md: '« PharFileInfo::isCompressed'
  - class.pharexception.md: PharException »
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::setMetadata'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharFileInfo::setMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::setMetadata — Встановлення метаданих для файлу

### Опис

```methodsynopsis
public PharFileInfo::setMetadata(mixed $metadata): void
```

**PharFileInfo::setMetadata()** слід використовувати для збереження метаданих конкретного файлу, які не можна зберігати всередині самого файлу, оскільки, якщо даних багато, або в принципі багато файлів з метаданими - це сповільнює завантаження phar-архіву. Важливо пам'ятати, що архіви з коробки підтримують права на файли і їх можна задати за допомогою методу [PharFileInfo::chmod()](pharfileinfo.chmod.md). Так як ця функціональність змінює phar-архів, необхідно, щоб опція [phar.readonly](phar.configuration.md#ini.phar.readonly) було відключено, інакше внести зміни до архіву [Phar](class.phar.md) не вийде. На архіви [PharData](class.phardata.md) обмеження на запис не поширюється.

Метадані файлів можна використовувати, наприклад, для вказівки, які права треба призначити файлу під час експорту його на диск, або для вказівки MIME-типу, який він повертає. Загалом - будь-яка корисна інформація, якій не місце всередині файлу.

### Список параметрів

`metadata`

Будь-яка змінна PHP, що містить необхідну інформацію

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** PharFileInfo::setMetadata()\*\*\*\*

```php
<?php
// удалим, на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.txt'] = 'hello';
    $p['file.txt']->setMetadata(array('user' => 'bill', 'mime-type' => 'text/plain'));
    var_dump($p['file.txt']->getMetaData());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить phar: ', $e;
}
?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  ["user"]=>
  string(4) "bill"
  ["mime-type"]=>
  string(10) "text/plain"
}
```

### Дивіться також

-   [PharFileInfo::hasMetadata()](pharfileinfo.hasmetadata.md) \- Перевірити, чи є у файлу метадані
-   [PharFileInfo::getMetadata()](pharfileinfo.getmetadata.md) \- Отримати метадані, пов'язані з файлом
-   [PharFileInfo::delMetadata()](pharfileinfo.delmetadata.md) \- Видалити метадані файлу
-   [Phar::setMetadata()](phar.setmetadata.md) \- Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.md) \- Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.md) \- Витягти метадані phar-архіву
