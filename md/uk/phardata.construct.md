Конструктор об'єкта PharData

-   [« PharData::compressFiles](phardata.compressfiles.md)
    
-   [PharData::convertToData »](phardata.converttodata.md)
    
-   [PHP Manual](index.md)
    
-   [PharData](class.phardata.md)
    
-   Конструктор об'єкта PharData
    

# PharData::construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::construct — Конструктор об'єкта PharData

### Опис

public **PharData::construct**  
string `$filename`  
int `$flags` = FilesystemIterator::SKIPDOTS | FilesystemIterator::UNIXPATHS,  
?string `$alias` **`null`**  
int `$format`

### Список параметрів

`filename`

Шлях або до існуючого tar/zip-архіву, або до новоствореного

`flags`

Прапори для передачі батьківському класу [Phar](class.phar.md) [RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)

`alias`

Псевдонім, який необхідно призначити phar-архіву для використання в потокових обгортках.

`format`

Одна з [констант формата файлов](phar.constants.html#phar.constants.fileformat) доступна для класу [Phar](class.phar.md)

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), якщо викликаний двічі; Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md)якщо Phar-архів неможливо відкрити.

### Приклади

**Приклад #1 Приклад використання **PharData::construct()****

```php
<?php
try {
    $p = new PharData('/path/to/my.tar', Phar::CURRENT_AS_FILEINFO | Phar::KEY_AS_FILENAME);
} catch (UnexpectedValueException $e) {
    die('Не удалось открыть my.tar');
} catch (BadMethodCallException $e) {
    echo 'Технически, это никогда не произойдёт';
}
echo file_get_contents('phar:///path/to/my.tar/example.txt');
?>
```