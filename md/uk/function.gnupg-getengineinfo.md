Повертає інформацію про двигун

-   [« gnupg\_export](function.gnupg-export.html)
    
-   [gnupg\_geterror »](function.gnupg-geterror.html)
    
-   [PHP Manual](index.html)
    
-   [GnuPG Функции](ref.gnupg.html)
    
-   Повертає інформацію про двигун
    

# gnupggetengineinfo

(PECL gnupg >= 1.5)

gnupggetengineinfo — Повертає інформацію про движок

### Опис

```methodsynopsis
gnupg_getengineinfo(resource $identifier): array
```

### Список параметрів

`identifier`

Ідентифікатор gnupg, отриманий з [gnupg\_init()](function.gnupg-init.html) або **gnupg**

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