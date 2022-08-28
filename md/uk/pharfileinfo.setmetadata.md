Встановлення метаданих для файлу

-   [« PharFileInfo::isCompressed](pharfileinfo.iscompressed.html)
    
-   [PharException »](class.pharexception.html)
    
-   [PHP Manual](index.html)
    
-   [PharFileInfo](class.pharfileinfo.html)
    
-   Встановлення метаданих для файлу
    

# PharFileInfo::setMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::setMetadata — Встановлення метаданих для файлу

### Опис

```methodsynopsis
public PharFileInfo::setMetadata(mixed $metadata): void
```

**PharFileInfo::setMetadata()** слід використовувати для збереження метаданих конкретного файлу, які не можна зберігати всередині самого файлу, оскільки, якщо даних багато, або в принципі багато файлів з метаданими - це сповільнює завантаження phar-архіву. Важливо пам'ятати, що архіви з коробки підтримують права на файли і їх можна задати за допомогою методу [PharFileInfo::chmod()](pharfileinfo.chmod.html). Так як ця функціональність змінює phar-архів, необхідно, щоб опція [phar.readonly](phar.configuration.html#ini.phar.readonly) було відключено, інакше внести зміни до архіву [Phar](class.phar.html) не вийде. На архіви [PharData](class.phardata.html) обмеження на запис не поширюється.

Метадані файлів можна використовувати, наприклад, для вказівки, які права треба призначити файлу під час експорту його на диск, або для вказівки MIME-типу, який він повертає. Загалом - будь-яка корисна інформація, якій не місце всередині файлу.

### Список параметрів

`metadata`

Будь-яка змінна PHP, що містить необхідну інформацію

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::setMetadata()****

```php
<?php
// удалим, на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.txt'] = 'hello';
    $p['file.txt']->setMetadata(array('user' => 'bill', 'mime-type' => 'text/plain'));
    var_dump($p['file.txt']->getMetaData());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить phar: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
array(2) {
  ["user"]=>
  string(4) "bill"
  ["mime-type"]=>
  string(10) "text/plain"
}
```

### Дивіться також

-   [PharFileInfo::hasMetadata()](pharfileinfo.hasmetadata.html) - Перевірити, чи є у файлу метадані
-   [PharFileInfo::getMetadata()](pharfileinfo.getmetadata.html) - Отримати метадані, пов'язані з файлом
-   [PharFileInfo::delMetadata()](pharfileinfo.delmetadata.html) - Видалити метадані файлу
-   [Phar::setMetadata()](phar.setmetadata.html) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.html) - Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.html) - Витягти метадані phar-архіву