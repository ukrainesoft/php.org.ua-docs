Створює жорстке посилання на файл

-   [« eioinit](function.eio-init.html)
    
-   [eiolstat »](function.eio-lstat.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Створює жорстке посилання на файл
    

# eiolink

(PECL eio >= 0.0.1dev)

eiolink — Створює жорстке посилання на файл

### Опис

```methodsynopsis
eio_link(    string $path,    string $new_path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiolink()** створює жорстке посилання `new_path` на файл, вказаний у `path`

### Список параметрів

`path`

Шлях до файлу.

`new_path`

Ім'я жорсткого заслання.

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.html)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **eiolink()****

```php
<?php
$filename = dirname(__FILE__)."/symlink.dat";
touch($filename);
$link = dirname(__FILE__)."/symlink.link";
$hardlink = dirname(__FILE__)."/hardlink.link";

function my_hardlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && !is_link($data));
    @unlink($data);

    eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_cb", $link);
}

function my_symlink_cb($data, $result) {
    global $link, $filename;
    var_dump(file_exists($data) && is_link($data));

    if (!eio_readlink($data, EIO_PRI_DEFAULT, "my_readlink_cb", NULL)) {
        @unlink($link);
        @unlink($filename);
    }
}

function my_readlink_cb($data, $result) {
    global $filename, $link;
    var_dump($result);

    @unlink($link);
    @unlink($filename);
}

eio_link($filename, $hardlink, EIO_PRI_DEFAULT, "my_hardlink_cb", $hardlink);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(true)
string(%d) "%ssymlink.dat"
```

### Дивіться також

-   [eiosymlink()](function.eio-symlink.html) - Створює символічне посилання