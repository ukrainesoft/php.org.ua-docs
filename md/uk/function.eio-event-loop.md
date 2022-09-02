---
navigation:
  - function.eio-dup2.md: « eiodup2
  - function.eio-fallocate.md: eiofallocate »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eioeventloop
---
# eioeventloop

(PECL eio >= 0.0.1dev)

eioeventloop — Взаємодіє з libeio доти, доки всі запити не будуть виконані

### Опис

```methodsynopsis
eio_event_loop(): bool
```

**eioeventloop()** взаємодіє з libeio до тих пір, поки всі запити не будуть виконані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eioeventloop()** повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **eioeventloop()****

```php
<?php
$temp_filename = "eio-temp-file.tmp";
touch($temp_filename);

/* Вызывается после выполнения eio_chmod() */
function my_chmod_callback($data, $result) {
    global $temp_filename;

    if ($result == 0 && !is_readable($temp_filename) && is_writable($temp_filename)) {
        echo "eio_chmod_ok";
    }

    @unlink($temp_filename);
}

eio_chmod($temp_filename, 0200, EIO_PRI_DEFAULT, "my_chmod_callback");
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
eio_chmod_ok
```

### Дивіться також

-   [eiopoll()](function.eio-poll.md) - Може бути викликана коли є запити, що очікують на виконання
