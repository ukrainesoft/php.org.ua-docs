Видалити метадані файлу

-   [« PharFileInfo::decompress](pharfileinfo.decompress.html)
    
-   [PharFileInfo::destruct »](pharfileinfo.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [PharFileInfo](class.pharfileinfo.html)
    
-   Видалити метадані файлу
    

# PharFileInfo::delMetadata

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.2.0)

PharFileInfo::delMetadata — Видалити метадані файлу

### Опис

```methodsynopsis
public PharFileInfo::delMetadata(): bool
```

Видаляє метадані файлу, якщо вони є.

### Список параметрів

Немає параметрів.

### Значення, що повертаються

Повертає **`true`** або **`false`** залежно від успішності виконання. Так як ця функціональність змінює phar-архів, необхідно, щоб опція [phar.readonly](phar.configuration.html#ini.phar.readonly) було відключено, інакше внести зміни до архіву [Phar](class.phar.html) не вийде. На архіви [PharData](class.phardata.html) обмеження на запис не поширюється.

### Помилки

Викидає виняток [PharException](class.pharexception.html) у разі виникнення помилки запису на диск, та [BadMethodCallException](class.badmethodcallexception.html), якщо запис заборонено.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::delMetaData()****

```php
<?php
try {
    $a = new Phar('myphar.phar');
    $a['hi'] = 'hi';
    var_dump($a['hi']->delMetadata());
    $a['hi']->setMetadata('there');
    var_dump($a['hi']->delMetadata());
    var_dump($a['hi']->delMetadata());
} catch (Exception $e) {
    // обработка ошибок
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

-   [PharFileInfo::setMetadata()](pharfileinfo.setmetadata.html) - Встановлення метаданих для конкретного файлу
-   [PharFileInfo::hasMetadata()](pharfileinfo.hasmetadata.html) - Перевірити, чи є у файлу метадані
-   [PharFileInfo::getMetadata()](pharfileinfo.getmetadata.html) - Отримати метадані, пов'язані з файлом
-   [Phar::setMetadata()](phar.setmetadata.html) - Встановити метадані phar-архіву
-   [Phar::hasMetadata()](phar.hasmetadata.html) - Перевірити, чи містить phar-архів глобальні метадані
-   [Phar::getMetadata()](phar.getmetadata.html) - Витягти метадані phar-архіву