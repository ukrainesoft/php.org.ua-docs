---
navigation:
  - function.eio-fchown.md: « eio\_fchown
  - function.eio-fstat.md: eio\_fstat »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fdatasync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fdatasync

(PECL eio >= 0.0.1dev)

eio\_fdatasync — Синхронізує стан файлу з фізичним пристроєм.

### Опис

```methodsynopsis
eio_fdatasync(    mixed $fd,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_fdatasync()** синхронізує поточний стан файлу із фізичним пристроєм.

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу, наприклад, повернутий [eio\_open()](function.eio-open.md)

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

**eio\_fdatasync()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
