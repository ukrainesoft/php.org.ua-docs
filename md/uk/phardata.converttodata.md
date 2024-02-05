---
navigation:
  - phardata.construct.md: '« PharData::\_\_construct'
  - phardata.converttoexecutable.md: 'PharData::convertToExecutable »'
  - index.md: PHP Manual
  - class.phardata.md: PharData
title: 'PharData::convertToData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PharData::convertToData

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::convertToData — Конвертація phar-архіву в tar/zip-архів, що не запускається.

### Опис

```methodsynopsis
public PharData::convertToData(?int $format = null, ?int $compression = null, ?string $extension = null): ?PharData
```

Цей метод використовується для перетворення tar/zip-архіву, що не запускається, в інший формат, що не запускається.

Якщо не вказано жодних змін, то буде викинуто виняток [BadMethodCallException](class.badmethodcallexception.md). Цей метод можна використовувати для перетворення tar-архіву на zip-архів і навпаки. Незважаючи на те, що можна змінити стиск для tar-архіву за допомогою цього методу, для цих цілей краще використовувати метод [PharData::compress()](phardata.compress.md)

У разі успішного виконання буде створено новий архів на диску та повернуто об'єкт [PharData](class.phardata.md). Старий архів не видалятиметься.

### Список параметрів

`format`

Одна из констант:`Phar::TAR`или`Phar::ZIP`. Якщо поставити як **`null`**, то буде використано поточний формат.

`compression`

Одна из констант:`Phar::NONE` (Для відключення стиснення всього архіву), `Phar::GZ`(для zlib-сжатия),`Phar::BZ2`(для bzip-сжатия).

`extension`

Цей параметр використовується для явної вказівки на розширення нового архіву. Зверніть увагу, що для архівів, що не запускаються, в жодному разі не можна допускати появу підрядка. `.phar`в любом месте имени файла.

По умолчанию для tar-архивов используются расширения:`.tar` `.tar.gz`и`.tar.bz2`. Для zip-архівів: `.zip`

### Значення, що повертаються

Метод повертає об'єкт [PharData](class.phardata.md)или\*\*`null`\*\*в случае возникновения ошибки.

### Помилки

Метод викидає виняток [BadMethodCallException](class.badmethodcallexception.md) коли не може зробити стискування, коли заданий невідомий метод стиснення, для архіву включена буферизація за допомогою [Phar::startBuffering()](phar.startbuffering.md), та не відключена за допомогою [Phar::stopBuffering()](phar.stopbuffering.md)Исключение[PharException](class.pharexception.md) викидається за будь-яких проблем створення phar-архіву.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `format` `compression`и`extension` тепер допускають значення null. |

### Приклади

**Пример #1 Пример использования**PharData::convertToData()\*\*\*\*

Використання PharData::convertToData():

```php
<?php
try {
    $tarphar = new PharData('myphar.tar');
    // обратите внимание, что myphar.tar *не* удаляется
    // создаём myphar.zip
    $zip = $tarphar->convertToData(Phar::ZIP);
    // создаём myphar.tbz
    $tgz = $zip->convertToData(Phar::TAR, Phar::BZ2, '.tbz');
    // создаём myphar.phar.tgz
    $phar = $tarphar->convertToData(Phar::PHAR); // выбрасывает исключение
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::convertToExecutable()](phar.converttoexecutable.md) \- Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.md) \- Конвертує phar-архів в tar-або zip-файл, що не виконується.
-   [PharData::convertToExecutable()](phardata.converttoexecutable.md) \- Конвертація tar/zip-архіву з даними в phar-архів, що запускається
