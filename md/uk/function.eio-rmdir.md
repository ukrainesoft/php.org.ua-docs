Видаляє директорію

-   [« eio\_rename](function.eio-rename.html)
    
-   [eio\_seek »](function.eio-seek.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Видаляє директорію
    

# eiormdir

(PECL eio >= 0.0.1dev)

eiormdir - Видаляє директорію

### Опис

```methodsynopsis
eio_rmdir(    string $path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiormdir()** видаляє директорію.

### Список параметрів

`path`

Шлях до директорії

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.html)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eiormdir()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **eiormdir()****

```php
<?php
$temp_dirname = "eio-temp-dir";
mkdir($temp_dirname);

function my_rmdir_callback($data, $result) {
    if ($result == 0 && !file_exists($data)) {
        echo "eio_rmdir_ok";
    } else if (file_exists($data)) {
        rmdir($data);
    }
}


eio_rmdir($temp_dirname, EIO_PRI_DEFAULT, "my_rmdir_callback", $temp_dirname);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
eio_rmdir_ok
```

### Дивіться також

-   [eio\_mkdir()](function.eio-mkdir.html) - створення директорії