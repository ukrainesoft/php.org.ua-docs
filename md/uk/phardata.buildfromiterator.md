---
navigation:
  - phardata.buildfromdirectory.md: '« PharData::buildFromDirectory'
  - phardata.compress.md: 'PharData::compress »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::buildFromIterator'
---
# PharData::buildFromIterator

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::buildFromIterator — Створення tar/zip-архіву за допомогою ітератора

### Опис

```methodsynopsis
public PharData::buildFromIterator(Traversable $iterator, ?string $baseDirectory = null): array
```

Заповнення архів tar або zip за допомогою ітератора. Підтримуються два типи ітераторів: ітератор, який зв'язує файл на диску з файлом усередині архіву та ітератор у стилі DirectoryIterator, який повертає об'єкти SplFileInfo. Для ітераторів, які повертають об'єкти SplFileInfo, другий параметр є обов'язковим.

### Список параметрів

`iterator`

Ітератор, що надає зв'язки ключ = значення, або об'єкти SplFileInfo

`baseDirectory`

Для ітераторів, що повертають об'єкти SplFileInfo, частина повного шляху файлів, що додаються, яка буде видалятися з повного шляху всередині архіву.

### Значення, що повертаються

**PharData::buildFromIterator()** повертає асоціативний масив, який пов'язує шлях до файлу всередині архіву з повним шляхом до файлу на диску.

### Помилки

Метод викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо ітератор повернув некоректне значення, наприклад, цілий ключ замість рядка. Виняток [BadMethodCallException](class.badmethodcallexception.md) викидається коли заданий ітератор, який повертає об'єкти SplFileInfo без завдання параметра `baseDirectory`. У разі проблем із записом на диск кидається виняток [PharException](class.pharexception.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | **PharData::buildFromIterator()** більше не повертає значення **`false`** |
|  | `baseDirectory` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **PharData::buildFromIterator()** з SplFileInfo**

Для більшості tar/zip-архівів, структура відображає дерево директорій на файловій системі. Наприклад, для створення tar/zip-архіву, що містить таку структуру директорій та файлів:

/path/to/project/ config/ dist.xml debug.xml lib/ file1.php file2.php src/ processthing.php www/ index.php cli/ index.php

Потрібно використовувати такий код для створення архіву "project.tar":

```php
<?php
$phar = new PharData('project.tar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new RecursiveDirectoryIterator('/path/to/project')),
    '/path/to/project');
?>
```

Файл `project.tar` можна використовувати одразу ж після його створення . **PharData::buildFromIterator()** не здійснює налаштування стиснення або додавання метаданих. Ці дії необхідно зробити самостійно після створення архіву.

Цікаве зауваження: **PharData::buildFromIterator()** також можна використовувати для копіювання контенту вже існуючого phar, tar або zip-архіву, так як об'єкт PharData успадковує [DirectoryIterator](class.directoryiterator.md)

```php
<?php
$phar = new PharData('project.tar');
$phar->buildFromIterator(
    new RecursiveIteratorIterator(
     new Phar('/path/to/anotherphar.phar')),
    'phar:///path/to/anotherphar.phar/path/to/project');
$phar->setStub($phar->createDefaultStub('cli/index.php', 'www/index.php'));
?>
```

**Приклад #2 Приклад використання **PharData::buildFromIterator()** з іншим ітератором**

Можна використовувати ітератори, що повертають зв'язку "ключ" => "значення", наприклад [ArrayIterator](class.arrayiterator.md)

```php
<?php
$phar = new PharData('project.tar');
$phar->buildFromIterator(
    new ArrayIterator(
     array(
        'internal/file.php' => dirname(__FILE__) . '/somefile.php',
        'another/file.jpg' => fopen('/path/to/bigfile.jpg', 'rb'),
     )));
?>
```

### Дивіться також

-   [Phar::buildFromIterator()](phar.buildfromiterator.md) - Створює phar-архів із ітератора
