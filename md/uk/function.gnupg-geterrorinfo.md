---
navigation:
  - function.gnupg-geterror.md: « gnupggeterror
  - function.gnupg-getprotocol.md: gnupggetprotocol »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupggeterrorinfo
---
# gnupggeterrorinfo

(PECL gnupg >= 1.5)

gnupggeterrorinfo — Повертає інформацію про помилку

### Опис

```methodsynopsis
gnupg_geterrorinfo(resource $identifier): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.md) або **gnupg**

### Значення, що повертаються

Повертає масив із інформацією про помилку.

### Приклади

**Приклад #1 Приклад використання **gnupggeterrorinfo()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
// вызывается без ошибок
print_r(gnupg_geterrorinfo($res));
?>
```

Результат виконання цього прикладу:

```
array(4) {
  ["generic_message"]=>
  bool(false)
  ["gpgme_code"]=>
  int(0)
  ["gpgme_source"]=>
  string(18) "Unspecified source"
  ["gpgme_message"]=>
  string(7) "Success"
}
```

**Приклад #2 Приклад використання **gnupggeterrorinfo()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg();
// вызов с ошибкой
$gpg->decrypt('abc');
// должна отобразиться информация об ошибке
print_r($gpg->geterrorinfo());
?>
```

Результат виконання цього прикладу:

```
array(4) {
  ["generic_message"]=>
  string(14) "decrypt failed"
  ["gpgme_code"]=>
  int(117440570)
  ["gpgme_source"]=>
  string(5) "GPGME"
  ["gpgme_message"]=>
  string(7) "No data"
}
```
