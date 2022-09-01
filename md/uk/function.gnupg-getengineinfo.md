---
navigation:
  - function.gnupg-export.html: « gnupgexport
  - function.gnupg-geterror.html: gnupggeterror »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupggetengineinfo
---
# gnupggetengineinfo

(PECL gnupg >= 1.5)

gnupggetengineinfo — Повертає інформацію про движок

### Опис

```methodsynopsis
gnupg_getengineinfo(resource $identifier): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupginit()](function.gnupg-init.html) або **gnupg**

### Значення, що повертаються

Повертає масив з інформацією про двигун, що складається з `protocol` `file_name` і `home_dir`

### Приклади

**Приклад #1 Приклад використання **gnupggetengineinfo()** у процедурному стилі**

```php
<?php
$res = gnupg_init();
print_r(gnupg_getengineinfo($res));
?>
```

Результат виконання цього прикладу:

```
array(3) {
  ["protocol"]=>
  int(0)
  ["file_name"]=>
  string(12) "/usr/bin/gpg"
  ["home_dir"]=>
  string(0) ""
}
```

**Приклад #2 Приклад використання **gnupggetengineinfo()** в об'єктно-орієнтованому стилі**

```php
<?php
$gpg = new gnupg(["file_name" => "/usr/bin/gpg2", "home_dir" => "/var/www/.gnupg"]);
print_r($gpg->getengineinfo());
?>
```

Результат виконання цього прикладу:

```
array(3) {
  ["protocol"]=>
  int(0)
  ["file_name"]=>
  string(13) "/usr/bin/gpg2"
  ["home_dir"]=>
  string(15) "/var/www/.gnupg"
}
```
