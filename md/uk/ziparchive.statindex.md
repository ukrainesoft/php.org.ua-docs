- [« ZipArchive::setPassword](ziparchive.setpassword.md)
- [ZipArchive::statName »](ziparchive.statname.md)

- [PHP Manual](index.md)
- [ZipArchive](class.ziparchive.md)
- отримання детальної інформації про елемент за його індексом

# ZipArchive::statIndex

(PHP 5 \>= 5.2.0, PHP 7, PHP 8, PECL zip \>= 1.1.0)

ZipArchive::statIndex — Отримання детальної інформації про його елемент
індексу

### Опис

public **ZipArchive::statIndex**(int `$index`, int `$flags` = 0):
array\|false

Отримання детальної інформації про елемент за його індексом.

### Список параметрів

`index`
Індекс елемент.

`flags`
**`ZipArchive::FL_UNCHANGED`** вказується на запит інформації
про вихідний файл в архіві, ігноруючи будь-які внесені зміни.

### Значення, що повертаються

Повертає масив, що містить детальну інформацію про елемент або
**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Отримання статистичної інформації про елемент**

` <?php$zip = new ZipArchive;$res = $zip->open('test.zip');if ($res === TRUE) {    print_r($zip->statIndex(3)); $zip->close();}else {    echo 'Помилка з кодом:' . $res;}?> `

Результатом виконання цього прикладу буде щось подібне:

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
