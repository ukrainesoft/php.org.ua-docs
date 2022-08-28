Змінює власника файлу

-   [« eio\_fchmod](function.eio-fchmod.html)
    
-   [eio\_fdatasync »](function.eio-fdatasync.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Змінює власника файлу
    

# eiofchown

(PECL eio >= 0.0.1dev)

eiofchown — Змінює власника файлу

### Опис

```methodsynopsis
eio_fchown(    mixed $fd,    int $uid,    int $gid = -1,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiofchown()** змінює власника файлу, дескриптор якого вказаний у `fd`

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

`uid`

Код користувача. Ігнорується при значенні, що дорівнює -1.

`gid`

Код групи. Ігнорується при значенні, що дорівнює -1.

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

[eio\_chmod()](function.eio-chmod.html) повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eio\_fchmod()](function.eio-fchmod.html) - Змінює права доступу до файлу