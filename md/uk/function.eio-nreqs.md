---
navigation:
  - function.eio-nready.md: « eio\_nready
  - function.eio-nthreads.md: eio\_nthreads »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_nreqs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_nreqs

(PECL eio >= 0.0.1dev)

eio\_nreqs — Повертає кількість запитів, які потрібно виконати

### Опис

```methodsynopsis
eio_nreqs(): int
```

**eio\_nreqs()** може бути виконана у довільному циклі, викликаному [eio\_poll()](function.eio-poll.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eio\_nreqs()** повертає кількість запитів, які потрібно виконати.

### Приклади

**Пример #1 Пример использования**eio\_nreqs()\*\*\*\*

```php
<?php
function res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

eio_nop(EIO_PRI_DEFAULT, "res_cb", "1");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "2");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "3");

while (eio_nreqs()) {
    eio_poll();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(1) "1"
int(0)
string(1) "3"
int(0)
string(1) "2"
int(0)
```

### Дивіться також

-   [eio\_poll()](function.eio-poll.md) \- Може бути викликана коли є запити, що очікують на виконання
-   [eio\_nready()](function.eio-nready.md) \- Повертає кількість ще не опрацьованих запитів
