---
navigation:
  - function.eio-busy.md: « eiobusy
  - function.eio-chmod.md: eiochmod »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiocancel
---
# eiocancel

(PECL eio >= 0.0.1dev)

eiocancel — Скасовує запит

### Опис

```methodsynopsis
eio_cancel(resource $req): void
```

**eiocancel()** скасовує запит, визначений у `req`

### Список параметрів

`req`

Ресурс запиту

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.md)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 **eiocancel()** example**

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

Результатом виконання цього прикладу буде щось подібне:

```
resource(4) of type (EIO Request Descriptor)
my_nop 2
```

### Дивіться також

-   [eiogrpcancel()](function.eio-grp-cancel.md) - Скасує групу запитів
