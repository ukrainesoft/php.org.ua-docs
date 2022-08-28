Синхронізує поточний стан файлу із фізичним пристроєм

-   [« eio\_fchown](function.eio-fchown.html)
    
-   [eio\_fstat »](function.eio-fstat.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Синхронізує поточний стан файлу із фізичним пристроєм
    

# eiofdatasync

(PECL eio >= 0.0.1dev)

eiofdatasync — Синхронізує стан файлу з фізичним пристроєм.

### Опис

```methodsynopsis
eio_fdatasync(    mixed $fd,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiofdatasync()** синхронізує поточний стан файлу із фізичним пристроєм.

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу, наприклад, повернутий [eio\_open()](function.eio-open.html)

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

**eiofdatasync()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.