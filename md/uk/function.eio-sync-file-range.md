Синхронізує сегмент файлу із даними файлу на зовнішньому сховищі

-   [« eiosymlink](function.eio-symlink.html)
    
-   [eiosync »](function.eio-sync.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Синхронізує сегмент файлу із даними файлу на зовнішньому сховищі
    

# eiosyncfilerange

(PECL eio >= 0.0.1dev)

eiosyncfilerange — Синхронізує сегмент файлу із даними файлу на зовнішньому сховищі

### Опис

```methodsynopsis
eio_sync_file_range(    mixed $fd,    int $offset,    int $nbytes,    int $flags,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiosyncfilerange()** здійснює необхідні перевірки та дії при синхронізації відкритого файлу `fd` з дисковою підсистемою.

### Список параметрів

`fd`

Файловий описувач

`offset`

Початкова позиція, з якою проводитиметься синхронізація

`nbytes`

Задає довжину сегмента файлу в байтах, яку потрібно синхронізувати. Якщо `nbytes` і нулю, будуть синхронізовані всі дані від `offset` до кінця файлу.

`flags`

Бітова маска. Може включати комбінацію з наступних значень: **`EIO_SYNC_FILE_RANGE_WAIT_BEFORE`** **`EIO_SYNC_FILE_RANGE_WRITE`** **`EIO_SYNC_FILE_RANGE_WAIT_AFTER`**. Ці прапори мають те саме призначення, що й аналогічні *SYNCFILERANGE* константи (дивіться сторінку керівництва `SYNC_FILE_RANGE(2)`

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

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eiosyncfilerange()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.