---
navigation:
  - phardata.addfromstring.md: '« PharData::addFromString'
  - phardata.buildfromiterator.md: 'PharData::buildFromIterator »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::buildFromDirectory'
---
# PharData::buildFromDirectory

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::buildFromDirectory — Створює tar/zip-архів із файлів у директорії

### Опис

```methodsynopsis
public PharData::buildFromDirectory(string $directory, string $pattern = ""): array
```

Наповнює tar/zip-архів вмістом директорії. Другий опціональний параметр є регулярним виразом (pcre). Файли, імена яких підходять під регулярне вираження, будуть включені в архів, а решта немає. Якщо при створенні архіву потрібна більша вибірковість, то використовуйте метод [PharData::buildFromIterator()](phardata.buildfromiterator.md)

### Список параметрів

`directory`

Повний або відносний шлях до директорії, файли з якої буде додано до архіву.

`pattern`

Регулярний вираз, який визначає, які файли необхідно включати в архів.

### Значення, що повертаються

[Phar::buildFromDirectory()](phar.buildfromdirectory.md) повертає асоціативний масив, що пов'язує шлях до файлу всередині архіву з повним шляхом до файлу на диску або **`false`** у разі виникнення помилки.

### Помилки

Викидає виняток [BadMethodCallException](class.badmethodcallexception.md)якщо не вдається ініціалізувати внутрішні ітератори директорії. Виняток [PharException](class.pharexception.md) викидається при помилках запису на диск.

### список змін

| Версия | Описание |
| --- | --- |
|  | **PharData::buildFromDirectory()** більше не повертає значення **`false`** |

### Приклади

**Приклад #1 Приклад використання **PharData::buildFromDirectory()****

```php
<?php
$phar = new PharData('project.tar');
// добавим все файлы в проект
$phar->buildFromDirectory(dirname(__FILE__) . '/project');

$phar2 = new PharData('project2.zip');
// добавим в проект только .php файлы
$phar2->buildFromDirectory(dirname(__FILE__) . '/project', '/\.php$/');
?>
```

### Дивіться також

-   [Phar::buildFromDirectory()](phar.buildfromdirectory.md) - Створює phar-архів із файлів, розташованих усередині директорії
-   [PharData::buildFromIterator()](phardata.buildfromiterator.md) - Створення tar/zip-архіву за допомогою ітератора
