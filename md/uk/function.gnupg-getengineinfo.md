---
navigation:
  - function.gnupg-export.md: « gnupg\_export
  - function.gnupg-geterror.md: gnupg\_geterror »
  - index.md: PHP Manual
  - ref.gnupg.md: GnuPG Функції
title: gnupg\_getengineinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gnupg\_getengineinfo

(PECL gnupg >= 1.5)

gnupg\_getengineinfo — Повертає інформацію про движок

### Опис

```methodsynopsis
gnupg_getengineinfo(resource $identifier): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.md)или**gnupg**

### Значення, що повертаються

Повертає масив з інформацією про двигун, що складається з `protocol` `file_name`и`home_dir`

### Приклади

**Пример #1 Пример использования**gnupg\_getengineinfo()\*\* у процедурному стилі\*\*

```php
<?php
$res = gnupg_init();
print_r(gnupg_getengineinfo($res));
?>
```

Результат виконання наведеного прикладу:

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

**Пример #2 Пример использования**gnupg\_getengineinfo()\*\* в об'єктно-орієнтованому стилі\*\*

```php
<?php
$gpg = new gnupg(["file_name" => "/usr/bin/gpg2", "home_dir" => "/var/www/.gnupg"]);
print_r($gpg->getengineinfo());
?>
```

Результат виконання наведеного прикладу:

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
