---
navigation:
  - function.eio-fsync.md: « eiofsync
  - function.eio-futime.md: eiofutime »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eioftruncate
---
# eioftruncate

(PECL eio >= 0.0.1dev)

eioftruncate — Зменшує розмір файлу

### Опис

```methodsynopsis
eio_ftruncate(    mixed $fd,    int $offset = 0,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eioftruncate()** урізує файл, дескриптор якого вказаний у параметрі `fd` точно до `length` байт.

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

`offset`

Зміщення від початку файлу

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
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

**eioftruncate()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eiotruncate()](function.eio-truncate.md) - Урізує розмір файлу
