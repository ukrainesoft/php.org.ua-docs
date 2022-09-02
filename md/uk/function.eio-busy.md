---
navigation:
  - ref.eio.md: « Eio Функции
  - function.eio-cancel.md: eiocancel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiobusy
---
# eiobusy

(PECL eio >= 0.0.1dev)

eiobusy - Штучно збільшує навантаження. Може бути корисним при тестуванні, вивченні продуктивності

### Опис

```methodsynopsis
eio_busy(    int $delay,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

Функція **eiobusy()** штучно збільшує навантаження, додаючи `delay` секунд до часу виконання. Корисно при налагодженні та тестуванні продуктивності.

### Список параметрів

`delay`

Затримка за секунди

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, або **`null`**. Якщо передано **`null`**, то `pri` встановлюється в **`EIO_PRI_DEFAULT`**

`callback`

Callback-функція, що виконується, коли всі запити групи будуть виконані.

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eiobusy()** повертає запит типу resource у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [eionop()](function.eio-nop.md) - Прохід по циклу запиту, не здійснюючи жодних операцій
