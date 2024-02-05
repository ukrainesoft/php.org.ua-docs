---
navigation:
  - function.eio-open.md: « eio\_open
  - function.eio-read.md: eio\_read »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_poll
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_poll

(PECL eio >= 0.0.1dev)

eio\_poll — Може бути викликана коли є запити, що очікують виконання

### Опис

```methodsynopsis
eio_poll(): int
```

**eio\_poll()** може бути використана для реалізації спеціальних циклів обробки запитів. При цьому [eio\_nreqs()](function.eio-nreqs.md) може бути використана для знаходження невиконаних запитів.

> **Зауваження** :
> 
> Застосовується тільки для реалізації циклу обробки запитів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо будь-який виклик запиту повертає ненульове значення, це повертається. Інакше повертає

### Приклади

**Приклад #1 Приклад використання** eio\_poll()\*\*\*\*

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

-   [eio\_nreqs()](function.eio-nreqs.md) \- Повертає кількість запитів, які потрібно виконати
