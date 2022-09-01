---
navigation:
  - ziparchive.setpassword.md: '« ZipArchive::setPassword'
  - ziparchive.statname.md: 'ZipArchive::statName »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::statIndex'
---
# ZipArchive::statIndex

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.1.0)

ZipArchive::statIndex — Отримання детальної інформації про елемент за його індексом

### Опис

```methodsynopsis
public ZipArchive::statIndex(int $index, int $flags = 0): array|false
```

Отримання детальної інформації про елемент за його індексом.

### Список параметрів

`index`

Індекс елемент.

`flags`

**`ZipArchive::FL_UNCHANGED`** вказується, щоб запитати інформацію про вихідний файл в архіві, ігноруючи будь-які зміни.

### Значення, що повертаються

Повертає масив, що містить детальну інформацію про елемент або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання статистичної інформації про елемент**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    print_r($zip->statIndex(3));
    $zip->close();
} else {
    echo 'Ошибка с кодом:' . $res;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [name] => foobar/baz
    [index] => 3
    [crc] => 499465816
    [size] => 27
    [mtime] => 1123164748
    [comp_size] => 24
    [comp_method] => 8
)
```
