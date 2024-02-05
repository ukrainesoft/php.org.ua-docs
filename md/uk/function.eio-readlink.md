---
navigation:
  - function.eio-readdir.md: « eio\_readdir
  - function.eio-realpath.md: eio\_realpath »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_readlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_readlink

(PECL eio >= 0.0.1dev)

eio\_readlink — Читає значення символічного посилання

### Опис

```methodsynopsis
eio_readlink(    string $path,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

### Список параметрів

`path`

Шлях до самого посилання

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

Дані, які потрібно передати у функцію `callback`

### Значення, що повертаються

**eio\_readlink()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_readlink()\*\*\*\*

```php
<?php
$filename = dirname(__FILE__)."/symlink.dat";
touch($filename);
$link = dirname(__FILE__)."/symlink.link";
$hardlink = dirname(__FILE__)."/hardlink.link";

function my_hardlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && !is_link($data));
    @unlink($data);

    eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_cb", $link);
}

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

eio_link($filename, $hardlink, EIO_PRI_DEFAULT, "my_hardlink_cb", $hardlink);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
string(16) "/tmp/symlink.dat"
```

### Дивіться також

-   [eio\_symlink()](function.eio-symlink.md) \- Створює символічне посилання
