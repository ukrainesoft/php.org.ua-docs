- [«eio_stat](function.eio-stat.md)
- [eio_symlink »](function.eio-symlink.md)

- [PHP Manual](index.md)
- [Eio Функції](ref.eio.md)
- Повертає статистику файлової системи

#eio_statvfs

(PECL eio \>= 0.0.1dev)

eio_statvfs — Повертає статистику файлової системи

### Опис

**eio_statvfs**(
string `$path`,
int `$pri`,
[callable](language.types.callable.md) `$callback`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`$ data` = ?
): resource

**eio_statvfs()** повертає статистику файлової системи до параметра
'result' функції 'callback'.

### Список параметрів

`path`
Ім'я будь-якого файлу у вмонтованій файловій системі.

`pri`
Пріоритет запитів: **`EIO_PRI_DEFAULT`**, **`EIO_PRI_MIN`**,
**`EIO_PRI_MAX`**, або **`null`**. Якщо переданий **`null`**, то `pri`
встановлюється у **`EIO_PRI_DEFAULT`**.

`callback`
Функція callback викликається при завершенні запиту. Вона повинна
задовольняти наступний прототип:

` void callback(mixed $data, int $result[, resource $req]);'

`data`
є даними користувача, переданими в запиті.

`result`
містить результуюче значення, що залежить від запиту; зазвичай це
значення, яке повертається відповідним системним викликом.

`req`
є опціональним запитуваним ресурсом, який може
використовуватися з такими функціями як
[eio_get_last_error()](function.eio-get-last-error.md)

`data`
Довільна змінна, що передається в `callback`-функцію.

### Значення, що повертаються

[eio_stat()](function.eio-stat.md) повертає покажчик на запит у
у разі успішного виконання або **`false`** у разі виникнення
помилки. У разі успішного виконання параметр 'result' функції
callback є масивом.

### Приклади

**Приклад #1 Приклад використання **eio_statvfs()****

` <?php$tmp_filename = '/tmp/eio-file.tmp';touch($tmp_filename);function my_statvfs_callback($data, $result) {    var_dump($data); var_dump($result); @unlink($data);}eio_statvfs($tmp_filename, EIO_PRI_DEFAULT, "my_statvfs_callback", $tmp_filename);eio_event_loop();?> `

Результатом виконання цього прикладу буде щось подібне:

string(17) "/tmp/eio-file.tmp"
array(11) {
["f_bsize"]=>
int(4096)
["f_frsize"]=>
int(4096)
["f_blocks"]=>
int(262144)
["f_bfree"]=>
int(262111)
["f_bavail"]=>
int(262111)
["f_files"]=>
int(1540815)
["f_ffree"]=>
int(1540743)
["f_favail"]=>
int(1540743)
["f_fsid"]=>
int(0)
["f_flag"]=>
int(4102)
["f_namemax"]=>
int(255)
}
