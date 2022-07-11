- [« Phar::copy](phar.copy.md)
- [Phar::createDefaultStub »](phar.createdefaultstub.md)

- [PHP Manual](index.md)
- [Phar](class.phar.md)
- Повертає кількість записів (файлів) у Phar-архіві

# Phar::count

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL phar = 1.0.0)

Phar::count — Повертає кількість записів (файлів) у Phar-архіві

### Опис

public **Phar::count**(int `$mode` = **`COUNT_NORMAL`**): int

### Список параметрів

### Значення, що повертаються

Кількість файлів, що містяться в цьому phar-архіві, або `0` (число
нуль), якщо архів порожній.

### Приклади

**Приклад #1 Приклад використання **Phar::count()****

`<?php// переконайтеся, що архів не існує@unlink('brandnewphar.phar');try {    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar','ar' ;} catch (Exception $e) {    echo 'Не удалося створити phar:', $e;}echo 'Новий phar містить ' . $p->count() . "записів
";$p['file.txt'] = 'привіт';echo 'Новий phar містить ' . $p->count() . "" записів
";?> `

Результат виконання цього прикладу:

Новий phar містить 0 записів
Новий phar містить 1 записів
