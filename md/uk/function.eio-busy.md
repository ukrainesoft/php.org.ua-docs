---
navigation:
  - ref.eio.md: « Eio Функції
  - function.eio-cancel.md: eio\_cancel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_busy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_busy

(PECL eio >= 0.0.1dev)

eio\_busy - Штучно збільшує навантаження. Може бути корисним при тестуванні, вивченні продуктивності

### Опис

```methodsynopsis
eio_busy(    int $delay,    int $pri = EIO_PRI_DEFAULT,    callable $callback = NULL,    mixed $data = NULL): resource
```

Функция\*\*eio\_busy()\*\*искусственно увеличивает нагрузку, добавляя`delay` секунд до часу виконання. Корисно при налагодженні та тестуванні продуктивності.

### Список параметрів

`delay`

Затримка за секунди

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, или\*\*`null`**. Якщо передано **`null`**, то`pri`устанавливается в**`EIO_PRI_DEFAULT`\*\*

`callback`

Callback-функція, що виконується, коли всі запити групи будуть виконані.

`data`

Произвольная переменная, передаваемая в`callback`\-функцію.

### Значення, що повертаються

**eio\_busy()** повертає запит типу resource у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [eio\_nop()](function.eio-nop.md) \- Прохід по циклу запиту, не здійснюючи жодних операцій
