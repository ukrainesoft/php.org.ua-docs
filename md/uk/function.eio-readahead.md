---
navigation:
  - function.eio-read.html: « eioread
  - function.eio-readdir.html: eioreaddir »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eioreadahead
---
# eioreadahead

(PECL eio >= 0.0.1dev)

eioreadahead — Поміщає дані з файлу до кешу сторінки

### Опис

```methodsynopsis
eio_readahead(    mixed $fd,    int $offset,    int $length,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eioreadahead()** заповнює кеш сторінки даними із файлу. Таким чином, подальші звернення до цього файлу не впливатимуть на роботу дискової підсистеми. Детальнішу інформацію можна отримати на сторінці посібника `READAHEAD(2)`

### Список параметрів

`fd`

Потік, ресурс сокету чи числовий файловий дескриптор.

`offset`

Позиція у файлі, з якою читатимуться дані.

`length`

Кількість байт, що зчитуються.

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

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.html)

`data`

Дані, які потрібно передати функції `callback`

### Значення, що повертаються

**eioreadahead()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.
