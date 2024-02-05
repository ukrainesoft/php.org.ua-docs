---
navigation:
  - function.eio-fstatvfs.md: « eio\_fstatvfs
  - function.eio-ftruncate.md: eio\_ftruncate »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fsync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fsync

(PECL eio >= 0.0.1dev)

eio\_fsync — Синхронізує стан файлу з фізичним пристроєм.

### Опис

```methodsynopsis
eio_fsync(    mixed $fd,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

Синхронізує поточний стан файлу із фізичним пристроєм.

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, или\*\*`null`**. Якщо передано **`null`**, то`pri`устанавливается в**`EIO_PRI_DEFAULT`\*\*

`callback`

Функция`callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.md)

`data`

Произвольная переменная, передаваемая в`callback`\-функцію.

### Значення, що повертаються

**eio\_fsync()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_sync()](function.eio-sync.md) \- Записує кеш із буфера на диск
