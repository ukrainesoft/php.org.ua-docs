---
navigation:
  - function.eio-fallocate.md: « eio\_fallocate
  - function.eio-fchown.md: eio\_fchown »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fchmod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fchmod

(PECL eio >= 0.0.1dev)

eio\_fchmod — Змінює права доступу до файлу

### Опис

```methodsynopsis
eio_fchmod(    mixed $fd,    int $mode,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

**eio\_fchmod()** змінює права доступу до файлу, дескриптор якого вказаний у `fd`

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу, наприклад, повернутий [eio\_open()](function.eio-open.md)

`mode`

Нові права доступу Наприклад, 0644.

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

**eio\_fchmod()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_fchown()](function.eio-fchown.md) \- Змінює власника файлу
