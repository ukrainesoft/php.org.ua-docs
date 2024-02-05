---
navigation:
  - function.eio-busy.md: « eio\_busy
  - function.eio-chmod.md: eio\_chmod »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_cancel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_cancel

(PECL eio >= 0.0.1dev)

eio\_cancel — Скасовує запит

### Опис

```methodsynopsis
eio_cancel(resource $req): void
```

**eio\_cancel()** скасовує запит, визначений у `req`

### Список параметрів

`req`

Ресурс запиту

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

Функція не повертає значення після виконання.

### Приклади

**Пример #1**eio\_cancel()**example**

```php
<?php
 /* Вызывается при завершении eio_nop() */
 function my_nop_cb($data, $result) {
  echo "my_nop ", $data, "\n";
 }

// Этот вызов eio_nop() будет отменён
$req = eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "1");
var_dump($req);
eio_cancel($req);

// Этот eio_nop() будет выполнен
eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "2");

// Выполнение запросов
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
resource(4) of type (EIO Request Descriptor)
my_nop 2
```

### Дивіться також

-   [eio\_grp\_cancel()](function.eio-grp-cancel.md) \- Скасує групу запитів
