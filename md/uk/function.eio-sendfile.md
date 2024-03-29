---
navigation:
  - function.eio-seek.md: « eio\_seek
  - function.eio-set-max-idle.md: eio\_set\_max\_idle »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_sendfile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_sendfile

(PECL eio >= 0.0.1dev)

eio\_sendfile — Переміщує дані між файлами

### Опис

```methodsynopsis
eio_sendfile(    mixed $out_fd,    mixed $in_fd,    int $offset,    int $length,    int $pri = ?,    callable $callback = ?,    string $data = ?): resource
```

**eio\_sendfile()** копіює дані з одного файлу до іншого. Дивіться додатковий опис `SENDFILE(2)`

### Список параметрів

`out_fd`

Вихідний потік, ресурс сокету чи дескриптор цільового файлу. Повинен бути відкритим для запису.

`in_fd`

Вхідний потік, ресурс сокету чи дескриптор файлу-джерела. Має бути відкритим для читання.

`offset`

Зміщення у файлі-джерелі.

`length`

Кількість байт, яке потрібно скопіювати.

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

Дані, які потрібно передати у функцію `callback`

### Значення, що повертаються

**eio\_sendfile()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
