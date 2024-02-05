---
navigation:
  - function.eio-fsync.md: « eio\_fsync
  - function.eio-futime.md: eio\_futime »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_ftruncate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_ftruncate

(PECL eio >= 0.0.1dev)

eio\_ftruncate — Зменшує розмір файлу

### Опис

```methodsynopsis
eio_ftruncate(    mixed $fd,    int $offset = 0,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_ftruncate()** урізує файл, дескриптор якого вказаний у параметрі `fd`точно до`length`байт.

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

`offset`

Зміщення від початку файлу

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

**eio\_ftruncate()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_truncate()](function.eio-truncate.md) \- Урізує розмір файлу
