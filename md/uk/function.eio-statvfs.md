---
navigation:
  - function.eio-stat.md: « eio\_stat
  - function.eio-symlink.md: eio\_symlink »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_statvfs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_statvfs

(PECL eio >= 0.0.1dev)

eio\_statvfs — Повертає статистику файлової системи

### Опис

```methodsynopsis
eio_statvfs(    string $path,    int $pri,    callable $callback,    mixed $data = ?): resource
```

**eio\_statvfs()** повертає статистику файлової системи до параметра `result` функції `callback`

### Список параметрів

`path`

Ім'я будь-якого файлу у вмонтованій файловій системі.

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, или\*\*`null`**. Якщо передано **`null`**, то`pri`устанавливается в**`EIO_PRI_DEFAULT`\*\*

`callback`

Функция`callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.md)

`data`

Произвольная переменная, передаваемая в`callback`\-функцію.

### Значення, що повертаються

[eio\_stat()](function.eio-stat.md) повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки. У разі успішного виконання параметр `result` функції `callback` є масивом.

### Приклади

**Приклад #1 Приклад використання** eio\_statvfs()\*\*\*\*

```php
<?php
$tmp_filename = '/tmp/eio-file.tmp';
touch($tmp_filename);

function my_statvfs_callback($data, $result) {
    var_dump($data);
    var_dump($result);

 @unlink($data);
}

eio_statvfs($tmp_filename, EIO_PRI_DEFAULT, "my_statvfs_callback", $tmp_filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
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
```
