---
navigation:
  - function.eio-seek.md: « eioseek
  - function.eio-set-max-idle.md: eiosetmaxidle »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiosendfile
---
# eiosendfile

(PECL eio >= 0.0.1dev)

eiosendfile — Переміщує дані між файлами

### Опис

```methodsynopsis
eio_sendfile(    mixed $out_fd,    mixed $in_fd,    int $offset,    int $length,    int $pri = ?,    callable $callback = ?,    string $data = ?): resource
```

**eiosendfile()** копіює дані з одного файлу до іншого. Дивіться додатковий опис `SENDFILE(2)`

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

Дані, які потрібно передати у функцію `callback`

### Значення, що повертаються

**eiosendfile()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.
