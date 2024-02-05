---
navigation:
  - function.eio-link.md: « eio\_link
  - function.eio-mkdir.md: eio\_mkdir »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_lstat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_lstat

(PECL eio >= 0.0.1dev)

eio\_lstat — Повертає статус файлу

### Опис

```methodsynopsis
eio_lstat(    string $path,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

**eio\_lstat()** повертає інформацію про стан файлу в `result`аргументе`callback`

### Список параметрів

`path`

Шлях до файлу

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

**eio\_lstat()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_lstat()\*\*\*\*

```php
<?php
$tmp_filename = dirname(__FILE__). "/eio-file.tmp";
touch($tmp_filename);

function my_res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

function my_open_cb($data, $result) {
    eio_close($result);
    eio_event_loop();

    @unlink($data);
}

eio_lstat($tmp_filename, EIO_PRI_DEFAULT, "my_res_cb", "eio_lstat");
eio_open($tmp_filename, EIO_O_RDONLY, NULL,
 EIO_PRI_DEFAULT, "my_open_cb", $tmp_filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(9) "eio_lstat"
array(12) {
 ["st_dev"]=>
  int(2050)
  ["st_ino"]=>
  int(2099197)
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
  int(1318235777)
  ["st_mtime"]=>
  int(1318235777)
  ["st_ctime"]=>
  int(1318235777)
}
```

### Дивіться також

-   [eio\_stat()](function.eio-stat.md) \- Повертає статус файлу
-   [eio\_fstat()](function.eio-fstat.md) \- Повертає статус файлу
