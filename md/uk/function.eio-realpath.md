Отримує абсолютний приведений до канонічного виду шлях

-   [« eio\_readlink](function.eio-readlink.html)
    
-   [eio\_rename »](function.eio-rename.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Отримує абсолютний приведений до канонічного виду шлях
    

# eiorealpath

(PECL eio >= 0.0.1dev)

eiorealpath - Отримує абсолютний приведений до канонічного виду шлях

### Опис

```methodsynopsis
eio_realpath(    string $path,    int $pri,    callable $callback,    string $data = NULL): resource
```

**eiorealpath()** повертає абсолютний шлях через аргумент `result` функції `callback`

### Список параметрів

`path`

Короткий чи відносний шлях

`pri`

`callback`

`data`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **eiorealpath()****

```php
<?php
var_dump(getcwd());

function my_realpath_allback($data, $result) {
    var_dump($result);
}

eio_realpath("../", EIO_PRI_DEFAULT, "my_realpath_allback");
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(12) "/home/ruslan"
string(5) "/home"
```