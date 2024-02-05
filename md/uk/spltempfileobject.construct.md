---
navigation:
  - class.spltempfileobject.md: « SplTempFileObject
  - spl.misc.md: Різні класи та інтерфейси »
  - index.md: PHP Manual
  - class.spltempfileobject.md: SplTempFileObject
title: 'SplTempFileObject::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplTempFileObject::\_\_construct

(PHP 5 >= 5.1.2, PHP 7, PHP 8)

SplTempFileObject::\_\_construct — Створює новий об'єкт тимчасового файлу

### Опис

public **SplTempFileObject::\_\_construct**(int`$maxMemory` \* \*

Створює новий об'єкт, який представляє тимчасовий файл.

### Список параметрів

`maxMemory`

Максимальний обсяг пам'яті (у байтах, за умовчанням дорівнює 2 МБ) для тимчасового файлу. Якщо тимчасовий файл перевищує цей розмір, він буде переміщений у файл у папці файлів тимчасових файлів.

Если значение`maxMemory` негативне, використовуватиметься лише пам'ять. Якщо значення `maxMemory` і нулю, то пам'ять не буде використовуватися.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md)в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SplTempFileObject()\*\*\*\*

Цей приклад створює в пам'яті тимчасовий файл, який можна записати дані і прочитати їх.

```php
<?php
$temp = new SplTempFileObject();
$temp->fwrite("Первая строка\n");
$temp->fwrite("А это вторая.\n");
echo "Во временный файл записано " . $temp->ftell() . " байт.\n\n";

// Перемотка в начало и чтение того, что было записано
$temp->rewind();
foreach ($temp as $line) {
    echo $line;
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Во временный файл записано 28 байт.

Первая строка
А это вторая.
```

### Дивіться також

-   [SplFileObject](class.splfileobject.md)
-   [потоки введення-виведення PHP](wrappers.php.md)(для`php://temp`и`php://memory`) .
