---
navigation:
  - function.eio-realpath.md: « eiorealpath
  - function.eio-rmdir.md: eiormdir »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiorename
---
# eiorename

(PECL eio >= 0.0.1dev)

eiorename — Змінює ім'я або переміщує файл

### Опис

```methodsynopsis
eio_rename(    string $path,    string $new_path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiorename()** здійснює переміщення чи перейменування файлу.

### Список параметрів

`path`

Початковий шлях до файлу

`new_path`

Кінцевий шлях до файлу під час переміщення

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.md)

`data`

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eiorename()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **eiorename()****

```php
<?php
$filename = dirname(__FILE__)."/eio-temp-file.dat";
touch($filename);
$new_filename = dirname(__FILE__)."/eio-temp-file-new.dat";

function my_rename_cb($data, $result) {
    global $filename, $new_filename;

    if ($result == 0 && !file_exists($filename) && file_exists($new_filename)) {
        @unlink($new_filename);
        echo "eio_rename_ok";
    } else {
        @unlink($filename);
    }
}

eio_rename($filename, $new_filename, EIO_PRI_DEFAULT, "my_rename_cb", $filename);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
eio_rename_ok
```
