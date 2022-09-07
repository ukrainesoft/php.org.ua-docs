---
navigation:
  - function.eio-statvfs.md: « eiostatvfs
  - function.eio-sync-file-range.md: eiosyncfilerange »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiosymlink
---
# eiosymlink

(PECL eio >= 0.0.1dev)

eiosymlink — Створює символічне посилання

### Опис

```methodsynopsis
eio_symlink(    string $path,    string $new_path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiosymlink()** створює символічне посилання `new_path` на шлях `path`

### Список параметрів

`path`

Шлях-джерело

`new_path`

Цільовий шлях

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.md)

`data`

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eiosymlink()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **eiosymlink()****

```php
<?php
$filename = dirname(__FILE__)."/symlink.dat";
touch($filename);
$link = dirname(__FILE__)."/symlink.link";

function my_symlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && is_link($data));

    if (!eio_readlink($data, EIO_PRI_DEFAULT, "my_readlink_cb", NULL)) {
        @unlink($link);
        @unlink($filename);
    }
}

function my_readlink_cb($data, $result) {
    global $filename, $link;
    var_dump($result);

    @unlink($link);
    @unlink($filename);
}

eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_cb", $link);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
string(16) "/tmp/symlink.dat"
```

### Дивіться також

-   [eiolink()](function.eio-link.md) - Створює жорстке посилання на файл
