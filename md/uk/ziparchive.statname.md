---
navigation:
  - ziparchive.statindex.md: '« ZipArchive::statIndex'
  - ziparchive.unchangeall.md: 'ZipArchive::unchangeAll »'
  - index.md: PHP Manual
  - class.ziparchive.md: ZipArchive
title: 'ZipArchive::statName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZipArchive::statName

(PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.5.0)

ZipArchive::statName — Отримання детальної інформації про елемент на ім'я

### Опис

```methodsynopsis
public ZipArchive::statName(string $name, int $flags = 0): array|false
```

Отримання детальної інформації про елемент на його ім'я.

### Список параметрів

`name`

Ім'я елемент.

`flags`

Прапор, що вказує, як має відбуватися пошук імені. Крім того, може вказуватися **`ZipArchive::FL_UNCHANGED`**, щоб запитати інформацію про вихідний файл в архіві, ігноруючи будь-які внесені зміни.

-   **`ZipArchive::FL_NOCASE`**
    
-   **`ZipArchive::FL_NODIR`**
    
-   **`ZipArchive::FL_UNCHANGED`**
    

### Значення, що повертаються

Повертає масив, що містить детальну інформацію про елемент або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання статистичної інформації про елемент**

```php
<?php
$zip = new ZipArchive;
$res = $zip->open('test.zip');
if ($res === TRUE) {
    print_r($zip->statName('foobar/baz'));
    $zip->close();
} else {
    echo 'Ошибка с кодом:' . $res;
}
?>
```

Висновок наведеного прикладу буде схожим на:

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
