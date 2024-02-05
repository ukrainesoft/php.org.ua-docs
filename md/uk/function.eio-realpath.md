---
navigation:
  - function.eio-readlink.md: « eio\_readlink
  - function.eio-rename.md: eio\_rename »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_realpath
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_realpath

(PECL eio >= 0.0.1dev)

eio\_realpath - Отримує абсолютний приведений до канонічного виду шлях

### Опис

```methodsynopsis
eio_realpath(    string $path,    int $pri,    callable $callback,    string $data = NULL): resource
```

**eio\_realpath()** повертає абсолютний шлях через аргумент `result` функції `callback`

### Список параметрів

`path`

Короткий чи відносний шлях

`pri`

`callback`

`data`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** eio\_realpath()\*\*\*\*

```php
<?php
var_dump(getcwd());

function my_realpath_allback($data, $result) {
    var_dump($result);
}

eio_realpath("../", EIO_PRI_DEFAULT, "my_realpath_allback");
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(12) "/home/ruslan"
string(5) "/home"
```
