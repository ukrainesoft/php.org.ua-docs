Конвертація tar/zip-архіву з даними в phar-архів, що запускається

-   [« PharData::convertToData](phardata.converttodata.html)
    
-   [PharData::copy »](phardata.copy.html)
    
-   [PHP Manual](index.html)
    
-   [PharData](class.phardata.html)
    
-   Конвертація tar/zip-архіву з даними в phar-архів, що запускається
    

# PharData::convertToExecutable

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

PharData::convertToExecutable — Конвертація tar/zip-архіву з даними в phar-архів, що запускається

### Опис

```methodsynopsis
public PharData::convertToExecutable(?int $format = null, ?int $compression = null, ?string $extension = null): ?Phar
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Цей метод використовується для конвертації tar/zip-архіву, що не запускається, а phar-архів, що запускається. Може бути використаний будь-який із трьох форматів, що запускаються (phar, tar або zip). Також допустимо стиснення архіву цілком.

Якщо зміни не вказані, цей метод кидає виняток [BadMethodCallException](class.badmethodcallexception.html)

У разі успішного виконання, цей метод створює новий архів на диску та повертає об'єкт [Phar](class.phar.html). Старий архів залишається недоторканим.

### Список параметрів

`format`

Одна з констант: `Phar::PHAR` `Phar::TAR`, або `Phar::ZIP`. Якщо поставлено **`null`**, буде збережено поточний формат.

`compression`

Одна з констант: `Phar::NONE` (без стиснення всього архіву), `Phar::GZ` (zlib стиск), `Phar::BZ2` (Bzip стиснення).

`extension`

Цей параметр використовується для явного завдання розширення нового архіву. Зверніть увагу, що для того, щоб оброблятися як phar-архів, файли мають у своєму розширенні мати `.phar`

При конвертації в phar-архіву, розширення за замовчуванням `.phar` `.phar.gz` або `.phar.bz2`, Залежно від заданого типу стиснення. Для tar-архівів, розширення за замовчуванням `.phar.tar` `.phar.tar.gz`, і `.phar.tar.bz2`. Для zip-архівів розширення за замовчуванням `.phar.zip`

### Значення, що повертаються

Цей метод повертає об'єкт [Phar](class.phar.html) і **`null`** у разі виникнення помилки.

### Помилки

Метод викидає виняток [BadMethodCallException](class.badmethodcallexception.html) якщо не може зробити стиснення або якщо заданий невідомий алгоритм стиснення, для архіву включена буферизація за допомогою [Phar::startBuffering()](phar.startbuffering.html), а метод [Phar::stopBuffering()](phar.stopbuffering.html) не викликався. Викидається виняток [UnexpectedValueException](class.unexpectedvalueexception.html), якщо запис заборонено. І викидається [PharException](class.pharexception.html), якщо виникли проблеми з записом на диск.

### список змін

| Версия | Описание                                                             |
|--------|----------------------------------------------------------------------|
|        | `format` `compression` і `localName` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **PharData::convertToExecutable()****

Використовуємо PharData::convertToExecutable():

```php
<?php
try {
    $tarphar = new PharData('myphar.tar');
    // конвертируем в формат phar
    // обратите внимание, что myphar.tar *не* удаляется
    $phar = $tarphar->convertToExecutable(Phar::PHAR); // creates myphar.phar
    $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
    // создаём myphar.phar.tgz
    $compressed = $tarphar->convertToExecutable(Phar::TAR, Phar::GZ, '.phar.tgz');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::convertToExecutable()](phar.converttoexecutable.html) - Конвертує phar-архів в інший формат файлу, що виконується.
-   [Phar::convertToData()](phar.converttodata.html) - Конвертує phar-архів в tar-або zip-файл, що не виконується.
-   [PharData::convertToData()](phardata.converttodata.html) - Конвертація phar-архіву в tar/zip-архів, що не запускається.