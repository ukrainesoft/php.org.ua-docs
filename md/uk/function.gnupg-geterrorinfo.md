---
navigation:
  - function.gnupg-geterror.md: « gnupg\_geterror
  - function.gnupg-getprotocol.md: gnupg\_getprotocol »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_geterrorinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_geterrorinfo

(PECL gnupg >= 1.5)

gnupg\_geterrorinfo — Повертає інформацію про помилку

### Опис

```methodsynopsis
gnupg_geterrorinfo(resource $identifier): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає масив із інформацією про помилку.

### Приклади

**Приклад #1 Приклад використання** gnupg\_geterrorinfo()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
// вызывается без ошибок
print_r(gnupg_geterrorinfo($res));
?>
```

Результат виконання наведеного прикладу:

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

**Приклад #2 Приклад використання** gnupg\_geterrorinfo()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg();
// вызов с ошибкой
$gpg->decrypt('abc');
// должна отобразиться информация об ошибке
print_r($gpg->geterrorinfo());
?>
```

Результат виконання наведеного прикладу:

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
