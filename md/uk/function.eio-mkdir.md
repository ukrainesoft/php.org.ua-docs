---
navigation:
  - function.eio-lstat.md: « eio\_lstat
  - function.eio-mknod.md: eio\_mknod »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_mkdir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_mkdir

(PECL eio >= 0.0.1dev)

eio\_mkdir - Створення директорії

### Опис

```methodsynopsis
eio_mkdir(    string $path,    int $mode,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_mkdir()** створює директорію із заданим режимом доступу `mode`

### Список параметрів

`path`

Шлях до нової директорії.

`mode`

Режим доступу, наприклад, 0755

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

Змінна, яку необхідно передати callback-функції `callback`

### Значення, що повертаються

У разі успішного виконання операції **eio\_mkdir()** поверне ресурс запиту або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** eio\_mkdir()\*\*\*\*

```php
<?php
$temp_dirname = "eio-temp-dir";

/* Вызывается, когда eio_mkdir() завершит работу */
function my_mkdir_callback($data, $result) {
 if ($result == 0 && is_dir($temp_dirname)
   && !is_readable($temp_dirname)
   && is_writable($temp_dirname)) {
  echo "eio_mkdir_ok";
 }

 // Удаляем директорию
    if (file_exists($data))
        rmdir($temp_dirname);
}

// Создаём директорию с режимом доступа 0300
eio_mkdir($temp_dirname, 0300, EIO_PRI_DEFAULT, "my_mkdir_callback", $temp_dirname);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
eio_mkdir_ok
```

### Дивіться також

-   [eio\_rmdir()](function.eio-rmdir.md) \- видаляє директорію
