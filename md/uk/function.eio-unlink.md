---
navigation:
  - function.eio-truncate.md: « eiotruncate
  - function.eio-utime.md: eioutime »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiounlink
---
# eiounlink

(PECL eio >= 0.0.1dev)

eiounlink — Видаляє файл або одне з жорстких посилань на нього

### Опис

```methodsynopsis
eio_unlink(    string $path,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiounlink()** видаляє ім'я із файлової системи.

### Список параметрів

`path`

Шлях до файлу

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

**eiounlink()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.
