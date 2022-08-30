Отримати метадані, пов'язані з файлом

-   [« PharFileInfo::getContent](pharfileinfo.getcontent.html)
    
-   [PharFileInfo::getPharFlags »](pharfileinfo.getpharflags.html)
    
-   [PHP Manual](index.html)
    
-   [PharFileInfo](class.pharfileinfo.html)
    
-   Отримати метадані, пов'язані з файлом
    

# PharFileInfo::getMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::getMetadata — Отримати метадані, пов'язані з файлом

### Опис

```methodsynopsis
public PharFileInfo::getMetadata(array $unserializeOptions = []): mixed
```

Повертає метадані, пов'язані з файлом.

### Список параметрів

### Значення, що повертаються

Будь-яка змінна PHP, яка може бути серіалізована та збережена у вигляді метаданих файлу, або \*\*`null`\*\*якщо метаданих немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `unserializeOptions` |

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::getMetadata()****

```php
<?php
// удалим, на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.txt'] = 'hello';
    $p['file.txt']->setMetadata(array('user' => 'bill', 'mime-type' => 'text/plain'));
    var_dump($p['file.txt']->getMetadata());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить brandnewphar.phar: ', $e;
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

-   [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.html) - Встановлення метаданих для конкретного файлу
-   [PharFileInfo::hasMetadata()](pharfileinfo.hasmetadata.html) - Перевірити, чи є у файлу метадані
-   [PharFileInfo::delMetadata()](pharfileinfo.delmetadata.html) - Видалити метадані файлу
-   [Phar::setMetadata()](phar.setmetadata.html) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.html) - Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.html) - Витягти метадані phar-архіву