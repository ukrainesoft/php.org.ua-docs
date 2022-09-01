---
navigation:
  - class.spltempfileobject.html: « SplTempFileObject
  - spl.misc.html: Різні класи та інтерфейси »
  - index.html: PHP Manual
  - class.spltempfileobject.html: SplTempFileObject
title: 'SplTempFileObject::construct'
---
# SplTempFileObject::construct

(PHP 5> = 5.1.2, PHP 7, PHP 8)

SplTempFileObject::construct — Створює новий об'єкт тимчасового файлу

### Опис

public **SplTempFileObject::construct**(int `$maxMemory`

Створює новий об'єкт, який представляє тимчасовий файл.

### Список параметрів

`maxMemory`

Максимальний обсяг пам'яті (у байтах, за умовчанням дорівнює 2 МБ) для тимчасового файлу. Якщо тимчасовий файл перевищує цей розмір, він буде переміщений у файл у папці тимчасових файлів.

Якщо значення `maxMemory` негативне, використовуватиметься лише пам'ять. Якщо значення `maxMemory` і нулю, то пам'ять не буде використовуватися.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.html) у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SplTempFileObject()****

Цей приклад створює в пам'яті тимчасовий файл, який можна записати дані і прочитати їх.

```php
<?php
$temp = new SplTempFileObject();
$temp->fwrite("Первая строка\n");
$temp->fwrite("А это вторая.\n");
echo "Во временный файл записано " . $temp->ftell() . " байт.\n\n";

// Перемотка в начало и чтение того, что было записано
$temp->rewind();
foreach ($temp as $line) {
    echo $line;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Во временный файл записано 28 байт.

Первая строка
А это вторая.
```

### Дивіться також

-   [SplFileObject](class.splfileobject.html)
-   [потоки введення-виведення PHP](wrappers.php.html) (для`php://temp` і `php://memory`
