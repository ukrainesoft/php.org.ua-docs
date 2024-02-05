---
navigation:
  - function.eio-mknod.md: « eio\_mknod
  - function.eio-npending.md: eio\_npending »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_nop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_nop

(PECL eio >= 0.0.1dev)

eio\_nop — Прохід циклу запиту, не виконуючи жодних операцій

### Опис

```methodsynopsis
eio_nop(int $pri = EIO_PRI_DEFAULT, callable $callback = NULL, mixed $data = NULL): resource
```

**eio\_nop()** проходить по циклу запиту, нічого при цьому не роблячи. Може виявитися корисною при налагодженні.

### Список параметрів

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

Дані, які будуть передані до `callback`\-функцію.

### Значення, що повертаються

**eio\_nop()** повертає ресурс запиту у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_busy()](function.eio-busy.md) \- Штучно збільшує навантаження. Може бути корисним при тестуванні, вивченні продуктивності
