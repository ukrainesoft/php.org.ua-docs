Створює дублікат дескриптора файлу

-   [« eio\_custom](function.eio-custom.html)
    
-   [eio\_event\_loop »](function.eio-event-loop.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Створює дублікат дескриптора файлу
    

# eiodup2

(PECL eio >= 0.0.1dev)

eiodup2 — Створює дублікат дескриптора файлу

### Опис

```methodsynopsis
eio_dup2(    mixed $fd,    mixed $fd2,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiodup2()** Створює дублікат дескриптора файлу.

### Список параметрів

`fd`

Вихідний потік, покажчик на сокет (Socket resource) або нумерований дескриптор файлу

`fd2`

Цільовий потік, покажчик на сокет (Socket resource) або нумерований дескриптор файлу

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

**eiodup2()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.