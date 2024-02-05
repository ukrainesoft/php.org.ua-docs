---
navigation:
  - function.eio-fstat.md: « eio\_fstat
  - function.eio-fsync.md: eio\_fsync »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fstatvfs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fstatvfs

(PECL eio >= 0.0.1dev)

eio\_fstatvfs — Повертає статистику файлової системи

### Опис

```methodsynopsis
eio_fstatvfs(    mixed $fd,    int $pri,    callable $callback,    mixed $data = ?): resource
```

**eio\_fstatvfs()** повертає статистику файлової системи в `result`аргумент`callback`

### Список параметрів

`fd`

Файловий дескриптор файлу вмонтованої файлової системи.

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

**eio\_fstatvfs()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_statvfs()](function.eio-statvfs.md) \- Повертає статистику файлової системи
