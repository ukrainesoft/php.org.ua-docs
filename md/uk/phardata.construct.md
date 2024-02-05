---
navigation:
  - phardata.compressfiles.md: '« PharData::compressFiles'
  - phardata.converttodata.md: 'PharData::convertToData »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::\_\_construct — Конструктор об'єкта PharData

### Опис

public **PharData::\_\_construct**  
string`$filename`,  
int`$flags`\= FilesystemIterator::SKIP\_DOTS | FilesystemIterator::UNIX\_PATHS,  
?string`$alias` **`null`**,  
int`$format`  
) .

### Список параметрів

`filename`

Шлях або до існуючого tar/zip-архіву, або до новоствореного

`flags`

Флаги для передачи родительскому классу[Phar](class.phar.md) [RecursiveDirectoryIterator](class.recursivedirectoryiterator.md)

`alias`

Псевдонім, який необхідно призначити phar-архіву для використання в потокових обгортках.

`format`

Одна из[констант формату файлів](phar.constants.md#phar.constants.fileformat)доступная для класса[Phar](class.phar.md)

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md), якщо викликаний двічі; Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md)якщо Phar-архів неможливо відкрити.

### Приклади

**Приклад #1 Приклад використання** PharData::\_\_construct()\*\*\*\*

```php
<?php
try {
    $p = new PharData('/path/to/my.tar', Phar::CURRENT_AS_FILEINFO | Phar::KEY_AS_FILENAME);
} catch (UnexpectedValueException $e) {
    die('Не удалось открыть my.tar');
} catch (BadMethodCallException $e) {
    echo 'Технически, это никогда не произойдёт';
}
echo file_get_contents('phar:///path/to/my.tar/example.txt');
?>
```
