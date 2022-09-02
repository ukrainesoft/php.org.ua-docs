---
navigation:
  - phar.converttodata.md: '« Phar::convertToData'
  - phar.copy.md: 'Phar::copy »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::convertToExecutable'
---
# Phar::convertToExecutable

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::convertToExecutable — Конвертує phar-архів в інший формат файлу.

### Опис

```methodsynopsis
public Phar::convertToExecutable(?int $format = null, ?int $compression = null, ?string $extension = null): ?Phar
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.md) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.md)

Цей метод використовується для конвертування phar-архіву в інший формат файлу. Наприклад, він може бути використаний для створення виконуваного phar-архіву, заснованого на tar, з виконуваного phar-архіву, заснованого на zip, або виконуваного phar-архіву з форматом файлу phar. Крім того, цей метод може бути використаний для стиснення цілого архіву, що базується на tar або phar.

Якщо не було вказано жодних змін, то даний метод викине виняток [BadMethodCallException](class.badmethodcallexception.md)

У разі успішного виконання цей метод створює на диску новий архів та повертає об'єкт [Phar](class.phar.md). Старий архів не видаляється з диска, це має бути зроблено вручну після завершення процесу.

### Список параметрів

`format`

Значенням цього параметра має бути одна з констант: `Phar::PHAR` `Phar::TAR` або `Phar::ZIP`. Якщо значення встановлено в **`null`**, то існуючий формат файлу буде збережено.

`compression`

Значенням цього параметра має бути одна з констант: `Phar::NONE` для відсутності стиску всього архіву, `Phar::GZ` для стиснення, заснованого на zlib, або `Phar::BZ2` для bzip-стискання.

`extension`

Цей параметр використовується для перевизначення розширення файлу за промовчанням для конвертованого архіву. Зверніть увагу, що всі phar-архіви, що базуються на tar або zip, повинні містити `.phar` у розширенні файлу щоб вони могли бути оброблені як phar-архів.

У разі конвертації архіву, заснованого на phar, розширеннями за умовчанням є `.phar` `.phar.gz` і `.phar.bz2`, Залежно від зазначеного стиснення. У разі конвертації phar-архіву, заснованого на tar, розширеннями за умовчанням є `.phar.tar` `.phar.tar.gz` і `.phar.tar.bz2`. Для архівів, що базуються на zip, розширенням за умовчанням є `.zip`

### Значення, що повертаються

Цей метод повертає об'єкт [Phar](class.phar.md) в успішного виконання та **`null`** у разі виникнення помилки.

### Помилки

Цей метод викидає виняток [BadMethodCallException](class.badmethodcallexception.md) у таких випадках: при неможливості стиснення; якщо було передано невідомий алгоритм стиснення; у запитаному архіві було включено буферизацію за допомогою [Phar::startBuffering()](phar.startbuffering.md) і не була завершена за допомогою [Phar::stopBuffering()](phar.stopbuffering.md). Якщо підтримка запису вимкнена, то буде кинуто виняток [UnexpectedValueException](class.unexpectedvalueexception.md). У разі виникнення будь-яких проблем у процесі створення phar викидається виняток [PharException](class.pharexception.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `format` `compression` і `localName` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::convertToExecutable()****

Використання Phar::convertToExecutable():

```php
<?php
try {
    $tarphar = new Phar('myphar.phar.tar');
    // конвертировать архив в формат phar
    // обратите внимание, что myphar.phar.tar *не* будет удалён
    $phar = $tarphar->convertToExecutable(Phar::PHAR); // будет создан myphar.phar
    $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
    // будет создан myphar.phar.tgz
    $compressed = $phar->convertToExecutable(Phar::TAR, Phar::GZ, '.phar.tgz');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::convertToData()](phar.converttodata.md) - Конвертує phar-архів в tar-або zip-файл, що не виконується.
-   [PharData::convertToExecutable()](phardata.converttoexecutable.md) - Конвертація tar/zip-архіву з даними в phar-архів, що запускається
-   [PharData::convertToData()](phardata.converttodata.md) - Конвертація phar-архіву в tar/zip-архів, що не запускається.
