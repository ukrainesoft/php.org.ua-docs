---
navigation:
  - function.eio-fstat.html: « eiofstat
  - function.eio-fsync.html: eiofsync »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiofstatvfs
---
# eiofstatvfs

(PECL eio >= 0.0.1dev)

eiofstatvfs — Повертає статистику файлової системи

### Опис

```methodsynopsis
eio_fstatvfs(    mixed $fd,    int $pri,    callable $callback,    mixed $data = ?): resource
```

**eiofstatvfs()** повертає статистику файлової системи в `result` аргумент `callback`

### Список параметрів

`fd`

Файловий дескриптор файлу вмонтованої файлової системи.

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.md)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eiofstatvfs()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eiostatvfs()](function.eio-statvfs.md) - Повертає статистику файлової системи
