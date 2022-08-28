Видалити файл із tar/zip-архіву

-   [« PharData::offsetSet](phardata.offsetset.html)
    
-   [PharData::setAlias »](phardata.setalias.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Видалити файл із tar/zip-архіву
    

# PharData::offsetUnset

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::offsetUnset — Видалити файл із tar/zip-архіву

### Опис

```methodsynopsis
public PharData::offsetUnset(string $localName): void
```

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.html), що дозволяє маніпулювати вмістом tar/zip-архіву у стилі доступу до елементів масиву. offsetUnset використовується для видалення файлів і запускається щоразу, коли використовується конструкція [unset()](function.unset.html)

### Список параметрів

`localName`

Назва файлу (відносний шлях).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [PharException](class.pharexception.html) у разі проблем із записом на диск.

### Приклади

**Приклад #1 Приклад використання **PharData::offsetUnset()****

```php
<?php
$p = new PharData('/path/to/my.zip');
try {
    // удаление file.txt из my.zip путём вызова offsetUnset
    unset($p['file.txt']);
} catch (Exception $e) {
    echo 'Не удалось удалить file.txt: ', $e;
}
?>
```

### Дивіться також

-   [Phar::offsetUnset()](phar.offsetunset.html) - Видалити файл із phar-архіву