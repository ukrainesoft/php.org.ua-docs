---
navigation:
  - phardata.iswritable.md: '« PharData::isWritable'
  - phardata.offsetunset.md: 'PharData::offsetUnset »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::offsetSet — Зміна вмісту файлу

### Опис

```methodsynopsis
public PharData::offsetSet(string $localName, resource|string $value): void
```

Це реалізація інтерфейсу [ArrayAccess](class.arrayaccess.md), що дозволяє маніпулювати вмістом tar/zip-архіву у стилі доступу до елементів масиву. offsetSet використовується для зміни контенту існуючого файлу або для створення нового.

### Список параметрів

`localName`

Ім'я файлу (відносний шлях).

`value`

Вміст файлу.

### Значення, що повертаються

Нічого не вертає.

### Помилки

Викидає виняток [PharException](class.pharexception.md)в случае проблем с записью на диск.

### Приклади

**Пример #1 Пример использования**PharData::offsetSet()\*\*\*\*

offsetSet не потрібно викликати безпосередньо. Використовуйте синтаксис `[]`

```php
<?php
$p = new PharData('/path/to/my.tar');
try {
    // вызов offsetSet
    $p['file.txt'] = 'Привет';
} catch (Exception $e) {
    echo 'Не удалось изменить file.txt:', $e;
}
?>
```

### Примітки

> **Зауваження** [PharData::addFile()](phardata.addfile.md) [PharData::addFromString()](phardata.addfromstring.md)and\*\*PharData::offsetSet()\*\*save a new phar archive each time they are called. If performance is a concern,[PharData::buildFromDirectory()](phardata.buildfromdirectory.md)or[PharData::buildFromIterator()](phardata.buildfromiterator.md)should be used instead.

### Дивіться також

-   [Phar::offsetSet()](phar.offsetset.md) \- Зміна вмісту файлу
