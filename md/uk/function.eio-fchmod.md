---
navigation:
  - function.eio-fallocate.md: « eiofallocate
  - function.eio-fchown.md: eiofchown »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiofchmod
---
# eiofchmod

(PECL eio >= 0.0.1dev)

eiofchmod — Змінює права доступу до файлу

### Опис

```methodsynopsis
eio_fchmod(    mixed $fd,    int $mode,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eiofchmod()** змінює права доступу до файлу, дескриптор якого вказаний у `fd`

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу, наприклад, повернутий [eioopen()](function.eio-open.md)

`mode`

Нові права доступу Наприклад, 0644.

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

**eiofchmod()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eiofchown()](function.eio-fchown.md) - Змінює власника файлу
