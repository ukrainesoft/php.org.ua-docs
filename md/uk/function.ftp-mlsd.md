- [«ftp_mkdir](function.ftp-mkdir.md)
- [ftp_nb_continue »](function.ftp-nb-continue.md)

- [PHP Manual](index.md)
- [Функції FTP](ref.ftp.md)
- Повертає список файлів у заданій директорії

#ftp_mlsd

(PHP 7 \>= 7.2.0, PHP 8)

ftp_mlsd — Повертає список файлів у заданій директорії

### Опис

**ftp_mlsd**([FTP\Connection](class.ftp-connection.md) `$ftp`, string
`$directory`): array\|false

### Список параметрів

`ftp`
An [FTP\Connection](class.ftp-connection.md) instance.

`directory`
Директорія, список файлів якої буде повернено.

### Значення, що повертаються

Повертає масив масивів з інформацією про файли із зазначеної
директорії у разі успішного виконання або **`false`** у разі
виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                                |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8.1.0  | Параметр ftp тепер чекає на екземпляр [FTP\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md)). |

### Приклади

**Приклад #1 Приклад використання **ftp_mlsd()****

`<?php// встановити основне з'єднання$ftp = ftp_connect($ftp_server);// авторизовуватися на сервері, використовуючи ім'я користувача і пароль$login_result = ftp_login$$$ $contents = ftp_mlsd($ftp, ".");// виведення $contentsvar_dump($contents);?> `

Результатом виконання цього прикладу буде щось подібне:

array(5) {
[0]=>
array(8) {
["name"]=>
string(1) "."
["modify"]=>
string(14) "20171212154511"
["perm"]=>
string(7) "flcdmpe"
["type"]=>
string(4) "cdir"
["unique"]=>
string(11) "811U5740002"
["UNIX.group"]=>
string(2) "33"
["UNIX.mode"]=>
string(4) "0755"
["UNIX.owner"]=>
string(2) "33"
}
[1]=>
array(8) {
["name"]=>
string(2) ".."
["modify"]=>
string(14) "20171212154511"
["perm"]=>
string(7) "flcdmpe"
["type"]=>
string(4) "pdir"
["unique"]=>
string(11) "811U5740002"
["UNIX.group"]=>
string(2) "33"
["UNIX.mode"]=>
string(4) "0755"
["UNIX.owner"]=>
string(2) "33"
}
[2]=>
array(8) {
["name"]=>
string(11) "public_html"
["modify"]=>
string(14) "20171211171525"
["perm"]=>
string(7) "flcdmpe"
["type"]=>
string(3) "dir"
["unique"]=>
string(11) "811U5740525"
["UNIX.group"]=>
string(2) "33"
["UNIX.mode"]=>
string(4) "0755"
["UNIX.owner"]=>
string(2) "33"
}
[3]=>
array(8) {
["name"]=>
string(10) "public_ftp"
["modify"]=>
string(14) "20171211174536"
["perm"]=>
string(7) "flcdmpe"
["type"]=>
string(3) "dir"
["unique"]=>
string(11) "811U57405EE"
["UNIX.group"]=>
string(2) "33"
["UNIX.mode"]=>
string(4) "0755"
["UNIX.owner"]=>
string(2) "33"
}
[4]=>
array(8) {
["name"]=>
string(3) "www"
["modify"]=>
string(14) "www"
["perm"]=>
string(7) "flcdmpe"
["type"]=>
string(3) "dir"
["unique"]=>
string(11) "811U5740780"
["UNIX.group"]=>
string(2) "33"
["UNIX.mode"]=>
string(4) "0755"
["UNIX.owner"]=>
string(2) "33"
}
}

### Дивіться також

- [ftp_rawlist()](function.ftp-rawlist.md) - Повертає докладний
список файлів у заданій директорії
- [ftp_nlist()](function.ftp-nlist.md) - Повертає список файлів у
заданої директорії
