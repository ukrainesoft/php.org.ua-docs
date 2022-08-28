Зміна вмісту файлу

-   [« PharData::isWritable](phardata.iswritable.html)
    
-   [PharData::offsetUnset »](phardata.offsetunset.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Зміна вмісту файлу
    

# PharData::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::offsetSet — Зміна вмісту файлу

### Опис

```methodsynopsis
public PharData::offsetSet(string $localName, resource|string $value): void
```

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.html), що дозволяє маніпулювати вмістом tar/zip-архіву у стилі доступу до елементів масиву. offsetSet використовується для зміни контенту існуючого файлу або для створення нового.

### Список параметрів

`localName`

Назва файлу (відносний шлях).

`value`

Вміст файлу.

### Значення, що повертаються

Нічого не вертає.

### Помилки

Викидає виняток [PharException](class.pharexception.html) у разі проблем із записом на диск.

### Приклади

**Приклад #1 Приклад використання **PharData::offsetSet()****

offsetSet не потрібно викликати безпосередньо. Використовуйте синтаксис `[]`

```php
<?php
$p = new PharData('/path/to/my.tar');
try {
    // вызов offsetSet
    $p['file.txt'] = 'Привет';
} catch (Exception $e) {
    echo 'Не удалось изменить file.txt:', $e;
}
?>
```

### Примітки

> **Зауваження** [PharData::addFile()](phardata.addfile.html) [PharData::addFromString()](phardata.addfromstring.html) and **PharData::offsetSet()** Залишити новий ріг архіву кожен час вони називаються. If performance is a concern, [PharData::buildFromDirectory()](phardata.buildfromdirectory.html) ор [PharData::buildFromIterator()](phardata.buildfromiterator.html) should be used instead.

### Дивіться також

-   [Phar::offsetSet()](phar.offsetset.html) - Зміна вмісту файлу