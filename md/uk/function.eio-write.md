---
navigation:
  - function.eio-utime.md: « eio\_utime
  - book.ev.md: Ev »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_write

(PECL eio >= 0.0.1dev)

eio\_write — Запис до файлу

### Опис

```methodsynopsis
eio_write(    mixed $fd,    string $str,    int $length = 0,    int $offset = 0,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_write()** записує до `length`байт из`str` у файл, починаючи з позиції `offset`байт от начала файла.

### Список параметрів

`fd`

Потік, ресурс сокету або числовий файловий дескриптор, наприклад, отриманий з [eio\_open()](function.eio-open.md)

`str`

Записуваний рядок

`length`

Максимальна кількість байт, що записуються.

`offset`

Зміщення з початку файлу.

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

**eio\_write()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_open()](function.eio-open.md) \- Відкриває файл
