Конвертація phar-архіву в tar/zip-архів, що не запускається.

-   [« PharData::construct](phardata.construct.html)
    
-   [PharData::convertToExecutable »](phardata.converttoexecutable.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Конвертація phar-архіву в tar/zip-архів, що не запускається.
    

# PharData::convertToData

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::convertToData — Конвертація phar-архіву в tar/zip-архів, що не запускається.

### Опис

```methodsynopsis
public PharData::convertToData(?int $format = null, ?int $compression = null, ?string $extension = null): ?PharData
```

Цей метод використовується для перетворення tar/zip-архіву, що не запускається, в інший формат, що не запускається.

Якщо не вказано жодних змін, то буде викинуто виняток [BadMethodCallException](class.badmethodcallexception.html). Цей метод можна використовувати для перетворення tar-архіву на zip-архів і навпаки. Незважаючи на те, що можна змінити стиск для tar-архіву за допомогою цього методу, для цих цілей краще використовувати метод [PharData::compress()](phardata.compress.html)

У разі успішного виконання буде створено новий архів на диску та повернуто об'єкт [PharData](class.phardata.html). Старий архів не видалятиметься.

### Список параметрів

`format`

Одна з констант: `Phar::TAR` або `Phar::ZIP`. Якщо поставити як **`null`**, то буде використано поточний формат.

`compression`

Одна з констант: `Phar::NONE` (Для відключення стиснення всього архіву), `Phar::GZ` (для zlib-стиснення), `Phar::BZ2` (Для bzip-стиснення).

`extension`

Цей параметр використовується для явної вказівки на розширення нового архіву. Зверніть увагу, що для архівів, що не запускаються, в жодному разі не можна допускати появу підрядка. `.phar` у будь-якому місці імені файлу.

За замовчуванням для tar-архівів використовуються розширення: `.tar` `.tar.gz` і `.tar.bz2`. Для zip-архівів: `.zip`

### Значення, що повертаються

Метод повертає об'єкт [PharData](class.phardata.html) або **`null`** у разі виникнення помилки.

### Помилки

Метод викидає виняток[BadMethodCallException](class.badmethodcallexception.html) коли не може зробити стискування, коли заданий невідомий метод стиснення, для архіву включена буферизація за допомогою [Phar::startBuffering()](phar.startbuffering.html), та не відключена за допомогою [Phar::stopBuffering()](phar.stopbuffering.html). Виняток [PharException](class.pharexception.html) викидається за будь-яких проблем створення phar-архіву.

### список змін

| Версия | Описание                                                             |
|--------|----------------------------------------------------------------------|
|        | `format` `compression` і `extension` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **PharData::convertToData()****

Використання PharData::convertToData():

```php
<?php
try {
    $tarphar = new PharData('myphar.tar');
    // обратите внимание, что myphar.tar *не* удаляется
    // создаём myphar.zip
    $zip = $tarphar->convertToData(Phar::ZIP);
    // создаём myphar.tbz
    $tgz = $zip->convertToData(Phar::TAR, Phar::BZ2, '.tbz');
    // создаём myphar.phar.tgz
    $phar = $tarphar->convertToData(Phar::PHAR); // выбрасывает исключение
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::convertToExecutable()](phar.converttoexecutable.html) - Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.html) - Конвертує phar-архів в tar-або zip-файл, що не виконується.
-   [PharData::convertToExecutable()](phardata.converttoexecutable.html) - Конвертація tar/zip-архіву з даними в phar-архів, що запускається