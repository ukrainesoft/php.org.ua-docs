---
navigation:
  - function.eio-nready.md: « eionready
  - function.eio-nthreads.md: eionthreads »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eionreqs
---
# eionreqs

(PECL eio >= 0.0.1dev)

eionreqs — Повертає кількість запитів, які потрібно виконати

### Опис

```methodsynopsis
eio_nreqs(): int
```

**eionreqs()** може бути виконана у довільному циклі, викликаному [eiopoll()](function.eio-poll.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eionreqs()** повертає кількість запитів, які потрібно виконати.

### Приклади

**Приклад #1 Приклад використання **eionreqs()****

```php
<?php
function res_cb($data, $result) {
    var_dump($data);
    var_dump($result);
}

eio_nop(EIO_PRI_DEFAULT, "res_cb", "1");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "2");
eio_nop(EIO_PRI_DEFAULT, "res_cb", "3");

while (eio_nreqs()) {
    eio_poll();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "1"
int(0)
string(1) "3"
int(0)
string(1) "2"
int(0)
```

### Дивіться також

-   [eiopoll()](function.eio-poll.md) - Може бути викликана коли є запити, що очікують на виконання
-   [eionready()](function.eio-nready.md) - Повертає кількість ще не опрацьованих запитів
