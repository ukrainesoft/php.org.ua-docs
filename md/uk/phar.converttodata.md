---
navigation:
  - phar.construct.md: '« Phar::construct'
  - phar.converttoexecutable.md: 'Phar::convertToExecutable »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::convertToData'
---
# Phar::convertToData

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::convertToData — Конвертує phar-архів у tar-або zip-файл, що не виконується.

### Опис

```methodsynopsis
public Phar::convertToData(?int $format = null, ?int $compression = null, ?string $extension = null): ?PharData
```

Цей метод використовується для конвертування phar-архів у tar- або zip-файл. Щоб створити зробити tar або zip нездійсненним, з створюваного в результаті конвертації архіву видаляються завантаження та псевдонім phar-архіву.

Якщо не було вказано жодних змін, то даний метод викине виняток [BadMethodCallException](class.badmethodcallexception.md)якщо формат файлу архіву є phar. У разі використання з архівами у форматі tar або zip, цей метод конвертує архів у архів, що не виконується.

У разі успішного виконання цей метод створює на диску новий архів та повертає об'єкт [PharData](class.phardata.md). Старий архів не видаляється з диска, це має бути зроблено вручну після завершення процесу.

### Список параметрів

`format`

Значенням цього параметра має бути одна з констант: `Phar::TAR` або `Phar::ZIP`. Якщо значення встановлено в **`null`**, то існуючий формат файлу буде збережено.

`compression`

Значенням цього параметра має бути одна з констант: `Phar::NONE` для відсутності стиску всього архіву, `Phar::GZ` для стиснення, заснованого на zlib, або `Phar::BZ2` для bzip-стискання.

`extension`

Цей параметр використовується для перевизначення розширення файлу за промовчанням для конвертованого архіву. Зверніть увагу, що `.phar` не може бути використано будь-де в імені файлу невиконуваного tar- або zip-архіву.

У разі конвертації phar-архіву, заснованого на tar, розширеннями за умовчанням є: `.tar` `.tar.gz` і `.tar.bz2`, Залежно від зазначеного стиснення. Для архівів, що базуються на zip, розширенням за умовчанням є `.zip`

### Значення, що повертаються

Цей метод повертає об'єкт [PharData](class.phardata.md) у разі успішного виконання та **`null`** у разі виникнення помилки.

### Помилки

Цей метод викидає виняток [BadMethodCallException](class.badmethodcallexception.md) у таких випадках: при неможливості стиснення; якщо було передано невідомий алгоритм стиснення; у запитаному архіві було включено буферизацію за допомогою [Phar::startBuffering()](phar.startbuffering.md) і не була завершена за допомогою [Phar::stopBuffering()](phar.stopbuffering.md). У разі виникнення будь-яких проблем у процесі створення phar буде викинуто виняток [PharException](class.pharexception.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `format` `compression` і `extension` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::convertToData()****

Використання Phar::convertToData():

```php
<?php
try {
    $tarphar = new Phar('myphar.phar.tar');
    // обратите внимание, что myphar.phar.tar *не* будет удалён
    // конверировать архив в неисполняемый tar-формат
    // будет создан myphar.tar
    $tar = $tarphar->convertToData();
    //  конверировать архив в неисполняемый zip-формат файла, будет создан myphar.zip
    $zip = $tarphar->convertToData(Phar::ZIP);
    // будет создан myphar.tbz
    $tgz = $tarphar->convertToData(Phar::TAR, Phar::BZ2, '.tbz');
    // будет создан myphar.phar.tgz
    $phar = $tarphar->convertToData(Phar::PHAR); // будет выброшено исключение
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::convertToExecutable()](phar.converttoexecutable.md) - Конвертує phar-архів в інший формат файлу, що виконується.
-   [PharData::convertToExecutable()](phardata.converttoexecutable.md) - Конвертація tar/zip-архіву з даними в phar-архів, що запускається
-   [PharData::convertToData()](phardata.converttodata.md) - Конвертація phar-архіву в tar/zip-архів, що не запускається.
