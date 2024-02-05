---
navigation:
  - function.eio-ftruncate.md: « eio\_ftruncate
  - function.eio-get-event-stream.md: eio\_get\_event\_stream »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_futime
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_futime

(PECL eio >= 0.0.1dev)

eio\_futime — Змінює дату та час останньої модифікації та доступу до файлу

### Опис

```methodsynopsis
eio_futime(    mixed $fd,    float $atime,    float $mtime,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_futime()** змінює дату та час останньої модифікації та доступу до файлу.

### Список параметрів

`fd`

Потік, покажчик на сокет, чи числовий дескриптор файлу, повернутий, наприклад, [eio\_open()](function.eio-open.md)

`atime`

Час останнього доступу

`mtime`

Час останньої зміни

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

**eio\_futime()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_utime()](function.eio-utime.md) \- Змінює дату та час останньої модифікації та доступу до файлу
