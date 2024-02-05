---
navigation:
  - function.eio-fchmod.md: « eio\_fchmod
  - function.eio-fdatasync.md: eio\_fdatasync »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fchown
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fchown

(PECL eio >= 0.0.1dev)

eio\_fchown — Змінює власника файлу

### Опис

```methodsynopsis
eio_fchown(    mixed $fd,    int $uid,    int $gid = -1,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_fchown()** змінює власника файлу, дескриптор якого вказаний у `fd`

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

`uid`

Код користувача. Ігнорується при значенні, що дорівнює -1.

`gid`

Код групи. Ігнорується при значенні, що дорівнює -1.

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

[eio\_chmod()](function.eio-chmod.md) повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_fchmod()](function.eio-fchmod.md) \- Змінює права доступу до файлу
