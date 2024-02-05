---
navigation:
  - function.eio-futime.md: « eio\_futime
  - function.eio-get-last-error.md: eio\_get\_last\_error »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_get\_event\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_get\_event\_stream

(PECL eio >= 0.3.1b)

eio\_get\_event\_stream - Повертає потік, що відображає змінну, що використовується при взаємодії з libeio

### Опис

```methodsynopsis
eio_get_event_stream(): mixed
```

**eio\_get\_event\_stream()** отримує потік, що відображає змінну, що використовується при взаємодії з libeio. Може бути використане для прив'язки деякого циклу обробки, що поставляється іншим модулем PECL, наприклад libevent.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eio\_get\_event\_stream()** повертає потік у разі успішного виконання або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Використання eio спільно з libevent**

```php
<?php
function my_eio_poll($fd, $events, $arg) {
    /* Некоторые действия с libevent могут быть здесь */
    if (eio_nreqs()) {
        eio_poll();
    }
    /* .. и здесь */
}

function my_res_cb($d, $r) {
    var_dump($r); var_dump($d);
}

$base = event_base_new();
$event = event_new();

$fd = eio_get_event_stream();
var_dump($fd);

eio_nop(EIO_PRI_DEFAULT, "my_res_cb", "nop data");
eio_mkdir("/tmp/abc-eio-temp", 0750, EIO_PRI_DEFAULT, "my_res_cb", "mkdir data");
/* Прочие eio_* запросы  ... */


// Установка флагов события
event_set($event, $fd, EV_READ /*| EV_PERSIST*/, "my_eio_poll", array($event, $base));

// Установка основы события
event_base_set($event, $base);

// Включение события
event_add($event);

// Запуск цикла обработки
event_base_loop($base);

/* То же самое доступно через интерфейс буфера libevent */
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
int(0)
string(8) "nop data"
int(0)
string(10) "mkdir data"
```
