---
navigation:
  - function.eio-set-min-parallel.html: « eiosetminparallel
  - function.eio-statvfs.html: eiostatvfs »
  - index.html: PHP Manual
  - ref.eio.html: Eio Функции
title: eioстати
---
# eioстати

(PECL eio >= 0.0.1dev)

eiostat — Повертає статус файлу

### Опис

```methodsynopsis
eio_stat(    string $path,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

**eioстати()** повертає інформацію про стан файлу в `result` аргумент функції `callback`

### Список параметрів

`path`

Шлях до файлу

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.html)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eioстати()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки. У разі успішного виконання параметр `result` функції `callback` є масивом.

### Приклади

**Приклад #1 Приклад використання **eioстати()****

```php
<?php
$tmp_filename = "eio-file.tmp";
touch($tmp_filename);

function my_res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

function my_open_cb($data, $result) {
    eio_close($result);
    eio_event_loop();

    @unlink($data);
}

eio_stat($tmp_filename, EIO_PRI_DEFAULT, "my_res_cb", "eio_stat");
eio_open($tmp_filename, EIO_O_RDONLY, NULL,
 EIO_PRI_DEFAULT, "my_open_cb", $tmp_filename);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(8) "eio_stat"
array(12) {
  ["st_dev"]=>
  int(2050)
  ["st_ino"]=>
  int(2489173)
  ["st_mode"]=>
  int(33188)
  ["st_nlink"]=>
  int(1)
  ["st_uid"]=>
  int(1000)
  ["st_gid"]=>
  int(100)
  ["st_rdev"]=>
  int(0)
  ["st_blksize"]=>
  int(4096)
  ["st_blocks"]=>
  int(0)
  ["st_atime"]=>
  int(1318250380)
  ["st_mtime"]=>
  int(1318250380)
  ["st_ctime"]=>
  int(1318250380)
}
```

### Дивіться також

-   [eiolstat()](function.eio-lstat.html) - Повертає статус файлу
-   [eiofstat()](function.eio-fstat.html) - Повертає статус файлу
