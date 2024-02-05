---
navigation:
  - phar.addemptydir.md: '« Phar::addEmptyDir'
  - phar.addfromstring.md: 'Phar::addFromString »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::addFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::addFile

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::addFile — Додає в phar-архів файл із файлової системи

### Опис

```methodsynopsis
public Phar::addFile(string $filename, ?string $localName = null): void
```

> **Зауваження** :
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly`в . В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

За допомогою цього методу phar-архів може бути доданий будь-який файл або вміст, доступний по URL. Якщо вказано необов'язковий другий параметр `localName`, то файл буде збережений в архіві з таким ім'ям, в іншому випадку як шлях для збереження всередині архіву буде використано параметр `file`При добавлении содержимого, доступного по URL, параметр`localname` має бути зазначено, інакше буде викинуто виняток. Цей метод аналогічний [ZipArchive::addFile()](ziparchive.addfile.md)

### Список параметрів

`filename`

Повний або відносний шлях до файлу у файловій системі, який має бути доданий до phar-архіву.

`localName`

Шлях, яким файл буде збережено в архіві.

### Значення, що повертаються

Немає значення, що повертається, у разі виникнення помилки викидається виняток.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `localName` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** Phar::addFile()\*\*\*\*

```php
<?php
try {
    $a = new Phar('/путь/к/phar.phar');

    $a->addFile('/полный/путь/к/файлу');
    // показывает, как хранится этот файл
    $b = $a['полный/путь/к/файлу']->getContent();

    $a->addFile('/полный/путь/к/файлу', 'моя_папка/file.txt');
    $c = $a['моя_папка/file.txt']->getContent();

    // показывает использоваие URL
    $a->addFile('http://www.example.com', 'example.md');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Примітки

> **Зауваження** **Phar::addFile()** [Phar::addFromString()](phar.addfromstring.md) і [Phar::offsetSet()](phar.offsetset.md) зберігає новий phar-архів щоразу під час їхнього виклику. Якщо продуктивність викликає занепокоєння, натомість слід використовувати [Phar::buildFromDirectory()](phar.buildfromdirectory.md) або [Phar::buildFromIterator()](phar.buildfromiterator.md)

### Дивіться також

-   [Phar::offsetSet()](phar.offsetset.md) \- Зміна вмісту файлу
-   [PharData::addFile()](phardata.addfile.md) \- Додати існуючі файли до tar/zip-архіву
-   [Phar::addFromString()](phar.addfromstring.md) \- Додає в phar-архів файл із рядка
-   [Phar::addEmptyDir()](phar.addemptydir.md) \- Додає в phar-архів порожню директорію
