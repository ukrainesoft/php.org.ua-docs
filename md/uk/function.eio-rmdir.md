---
navigation:
  - function.eio-rename.md: « eio\_rename
  - function.eio-seek.md: eio\_seek »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_rmdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_rmdir

(PECL eio >= 0.0.1dev)

eio\_rmdir - Видаляє директорію

### Опис

```methodsynopsis
eio_rmdir(    string $path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_rmdir()** видаляє директорію.

### Список параметрів

`path`

Шлях до директорії

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

**eio\_rmdir()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_rmdir()\*\*\*\*

```php
<?php
$temp_dirname = "eio-temp-dir";
mkdir($temp_dirname);

function my_rmdir_callback($data, $result) {
    if ($result == 0 && !file_exists($data)) {
        echo "eio_rmdir_ok";
    } else if (file_exists($data)) {
        rmdir($data);
    }
}


eio_rmdir($temp_dirname, EIO_PRI_DEFAULT, "my_rmdir_callback", $temp_dirname);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
eio_rmdir_ok
```

### Дивіться також

-   [eio\_mkdir()](function.eio-mkdir.md) \- створення директорії
