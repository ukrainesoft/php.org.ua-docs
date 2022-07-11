- [«gnupg_geterror](function.gnupg-geterror.md)
- [gnupg_getprotocol »](function.gnupg-getprotocol.md)

- [PHP Manual](index.md)
- [GnuPG Функції](ref.gnupg.md)
- Повертає інформацію про помилку

#gnupg_geterrorinfo

(PECL gnupg \>= 1.5)

gnupg_geterrorinfo — Повертає інформацію про помилку

### Опис

**gnupg_geterrorinfo**(resource `$identifier`): array

### Список параметрів

`identifier`
Ідентифікатор gnupg, отриманий з
[gnupg_init()](function.gnupg-init.md) або **gnupg**.

### Значення, що повертаються

Повертає масив із інформацією про помилку.

### Приклади

**Приклад #1 Приклад використання **gnupg_geterrorinfo()** у процедурному
стилі**

` <?php$res = gnupg_init();// викликається без помилокprint_r(gnupg_geterrorinfo($res));?> `

Результат виконання цього прикладу:

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

**Приклад #2 Приклад використання **gnupg_geterrorinfo()** в
об'єктно-орієнтованому стилі**

`<?php$gpg = new gnupg();// виклик з помилкою$gpg->decrypt('abc');// повинна відобразитися інформація про помилкаprint_r($gpg->geterrorinfo()

Результат виконання цього прикладу:

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
