---
navigation:
  - function.eio-realpath.md: « eio\_realpath
  - function.eio-rmdir.md: eio\_rmdir »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_rename

(PECL eio >= 0.0.1dev)

eio\_rename — Змінює ім'я або переміщує файл

### Опис

```methodsynopsis
eio_rename(    string $path,    string $new_path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_rename()** здійснює переміщення чи перейменування файлу.

### Список параметрів

`path`

Початковий шлях до файлу

`new_path`

Кінцевий шлях до файлу під час переміщення

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

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eio\_rename()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_rename()\*\*\*\*

```php
<?php
$filename = dirname(__FILE__)."/eio-temp-file.dat";
touch($filename);
$new_filename = dirname(__FILE__)."/eio-temp-file-new.dat";

function my_rename_cb($data, $result) {
    global $filename, $new_filename;

    if ($result == 0 && !file_exists($filename) && file_exists($new_filename)) {
        @unlink($new_filename);
        echo "eio_rename_ok";
    } else {
        @unlink($filename);
    }
}

eio_rename($filename, $new_filename, EIO_PRI_DEFAULT, "my_rename_cb", $filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
eio_rename_ok
```
