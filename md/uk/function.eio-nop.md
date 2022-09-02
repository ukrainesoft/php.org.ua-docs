---
navigation:
  - function.eio-mknod.md: « eiomknod
  - function.eio-npending.md: eionpending »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eionop
---
# eionop

(PECL eio >= 0.0.1dev)

eionop — Прохід циклу запиту, не виконуючи жодних операцій

### Опис

```methodsynopsis
eio_nop(int $pri = EIO_PRI_DEFAULT, callable $callback = NULL, mixed $data = NULL): resource
```

**eionop()** проходить по циклу запиту, нічого при цьому не роблячи. Може виявитися корисною при налагодженні.

### Список параметрів

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

Дані, які будуть передані до `callback`функцію.

### Значення, що повертаються

**eionop()** повертає ресурс запиту у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eiobusy()](function.eio-busy.md) - Штучно збільшує навантаження. Може бути корисним при тестуванні, вивченні продуктивності
