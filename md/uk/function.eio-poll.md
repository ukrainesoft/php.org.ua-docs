---
navigation:
  - function.eio-open.md: « eioopen
  - function.eio-read.md: eioread »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiopoll
---
# eiopoll

(PECL eio >= 0.0.1dev)

eiopoll — Може бути викликана коли є запити, що очікують виконання

### Опис

```methodsynopsis
eio_poll(): int
```

**eiopoll()** може бути використана для реалізації спеціальних циклів обробки запитів. При цьому [eionreqs()](function.eio-nreqs.md) може бути використана для знаходження невиконаних запитів.

> **Зауваження**
> 
> Застосовується тільки для реалізації циклу обробки запитів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо будь-який виклик запиту повертає ненульове значення, це повертається. Інакше повертає **`0`**

### Приклади

**Приклад #1 Приклад використання **eiopoll()****

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
    // Некоторый специфичный IPC или что-то ещё
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

-   [eionreqs()](function.eio-nreqs.md) - Повертає кількість запитів, які потрібно виконати
