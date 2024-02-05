---
navigation:
  - function.eio-dup2.md: « eio\_dup2
  - function.eio-fallocate.md: eio\_fallocate »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_event\_loop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_event\_loop

(PECL eio >= 0.0.1dev)

eio\_event\_loop — Взаємодіє з libeio доти, доки всі запити не будуть виконані

### Опис

```methodsynopsis
eio_event_loop(): bool
```

**eio\_event\_loop()** взаємодіє з libeio до тих пір, поки всі запити не будуть виконані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eio\_event\_loop()** повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_event\_loop()\*\*\*\*

```php
<?php
$temp_filename = "eio-temp-file.tmp";
touch($temp_filename);

/* Вызывается после выполнения eio_chmod() */
function my_chmod_callback($data, $result) {
    global $temp_filename;

    if ($result == 0 && !is_readable($temp_filename) && is_writable($temp_filename)) {
        echo "eio_chmod_ok";
    }

    @unlink($temp_filename);
}

eio_chmod($temp_filename, 0200, EIO_PRI_DEFAULT, "my_chmod_callback");
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
eio_chmod_ok
```

### Дивіться також

-   [eio\_poll()](function.eio-poll.md) \- Може бути викликана коли є запити, що очікують на виконання
