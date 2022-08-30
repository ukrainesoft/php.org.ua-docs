Отримати прапори файлу в phar-архіві

-   [« PharFileInfo::getMetadata](pharfileinfo.getmetadata.md)
    
-   [PharFileInfo::hasMetadata »](pharfileinfo.hasmetadata.md)
    
-   [PHP Manual](index.md)
    
-   [PharFileInfo](class.pharfileinfo.md)
    
-   Отримати прапори файлу в phar-архіві
    

# PharFileInfo::getPharFlags

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::getPharFlags — Отримати прапори файлу в phar-архіві

### Опис

```methodsynopsis
public PharFileInfo::getPharFlags(): int
```

Повертає набір прапорів, заданих у маніфесті Phar-архіву. У поточній реалізації завжди повертає `0`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Прапори Phar-архіву (поки що завжди `0`

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::getPharFlags()****

```php
<?php
try {
    $p = new Phar('/path/to/my.phar', 0, 'my.phar');
    $p['myfile.txt'] = 'hi';
    $file = $p['myfile.txt'];
    var_dump($file->getPharFlags());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить my.phar: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
int(0)
```