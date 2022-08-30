Запис у файл

-   [« eioutime](function.eio-utime.html)
    
-   [Ev »](book.ev.md)
    
-   [PHP Manual](index.md)
    
-   [Eio Функции](ref.eio.md)
    
-   Запис у файл
    

# eiowrite

(PECL eio >= 0.0.1dev)

eiowrite — Запис до файлу

### Опис

```methodsynopsis
eio_write(    mixed $fd,    string $str,    int $length = 0,    int $offset = 0,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiowrite()** записує до `length` байт з `str` у файл, починаючи з позиції `offset` байт з початку файла.

### Список параметрів

`fd`

Потік, ресурс сокету або числовий файловий дескриптор, наприклад, отриманий з [eioopen()](function.eio-open.html)

`str`

Записуваний рядок

`length`

Максимальна кількість байт, що записуються.

`offset`

Зміщення з початку файла.

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

Дані, які потрібно передати у функцію `callback`

### Значення, що повертаються

**eiowrite()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eioopen()](function.eio-open.html) - Відкриває файл