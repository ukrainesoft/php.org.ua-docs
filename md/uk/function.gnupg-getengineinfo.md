- [«gnupg_export](function.gnupg-export.md)
- [gnupg_geterror »](function.gnupg-geterror.md)

- [PHP Manual](index.md)
- [GnuPG Функції](ref.gnupg.md)
- Повертає інформацію про движок

#gnupg_getengineinfo

(PECL gnupg \>= 1.5)

gnupg_getengineinfo — Повертає інформацію про движок

### Опис

**gnupg_getengineinfo**(resource `$identifier`): array

### Список параметрів

`identifier`
Ідентифікатор gnupg, отриманий з
[gnupg_init()](function.gnupg-init.md) або **gnupg**.

### Значення, що повертаються

Повертає масив з інформацією про двигун, що складається з `protocol`,
`file_name` та `home_dir`.

### Приклади

**Приклад #1 Приклад використання **gnupg_getengineinfo()** у процедурному
стилі**

` <?php$res = gnupg_init();print_r(gnupg_getengineinfo($res));?> `

Результат виконання цього прикладу:

array(3) {
["protocol"]=>
int(0)
["file_name"]=>
string(12) "/usr/bin/gpg"
["home_dir"]=>
string(0) ""
}

**Приклад #2 Приклад використання **gnupg_getengineinfo()** в
об'єктно-орієнтованому стилі**

` <?php$gpg = new gnupg(["file_name" => "/usr/bin/gpg2", "home_dir" => "/var/www/.gnupg"]);print_r($gpg->getengineinfo( ));?> `

Результат виконання цього прикладу:

array(3) {
["protocol"]=>
int(0)
["file_name"]=>
string(13) "/usr/bin/gpg2"
["home_dir"]=>
string(15) "/var/www/.gnupg"
}
