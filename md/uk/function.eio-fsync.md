---
navigation:
  - function.eio-fstatvfs.html: « eiofstatvfs
  - function.eio-ftruncate.html: eioftruncate »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiofsync
---
# eiofsync

(PECL eio >= 0.0.1dev)

eiofsync — Синхронізує поточний стан файлу із фізичним пристроєм.

### Опис

```methodsynopsis
eio_fsync(    mixed $fd,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

Синхронізує поточний стан файлу із фізичним пристроєм.

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

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

**eiofsync()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eiosync()](function.eio-sync.html) - Записує кеш із буфера на диск
