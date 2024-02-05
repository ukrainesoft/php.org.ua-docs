---
navigation:
  - function.eio-read.md: « eio\_read
  - function.eio-readdir.md: eio\_readdir »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_readahead
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_readahead

(PECL eio >= 0.0.1dev)

eio\_readahead — Поміщає дані з файлу до кешу сторінки

### Опис

```methodsynopsis
eio_readahead(    mixed $fd,    int $offset,    int $length,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_readahead()** заповнює кеш сторінки даними із файлу. Таким чином, подальші звернення до цього файлу не впливатимуть на роботу дискової підсистеми. Детальнішу інформацію можна отримати на сторінці посібника `READAHEAD(2)`

### Список параметрів

`fd`

Потік, ресурс сокету чи числовий файловий дескриптор.

`offset`

Позиція у файлі, з якою читатимуться дані.

`length`

Кількість байт, що зчитуються.

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

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eio\_readahead()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
