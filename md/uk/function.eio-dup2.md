---
navigation:
  - function.eio-custom.md: « eio\_custom
  - function.eio-event-loop.md: eio\_event\_loop »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_dup2
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_dup2

(PECL eio >= 0.0.1dev)

eio\_dup2 — Створює дублікат дескриптора файлу

### Опис

```methodsynopsis
eio_dup2(    mixed $fd,    mixed $fd2,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_dup2()** Створює дублікат дескриптора файлу.

### Список параметрів

`fd`

Вихідний потік, покажчик на сокет (Socket resource) або нумерований дескриптор файлу

`fd2`

Цільовий потік, покажчик на сокет (Socket resource), або нумерований дескриптор файлу

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

**eio\_dup2()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
