Повертає потік, що відображає змінну, що використовується при взаємодії з libeio

-   [« eio\_futime](function.eio-futime.html)
    
-   [eio\_get\_last\_error »](function.eio-get-last-error.html)
    
-   [PHP Manual](index.html)
    
-   [Eio Функции](ref.eio.html)
    
-   Повертає потік, що відображає змінну, що використовується при взаємодії з libeio
    

# eiogeteventstream

(PECL eio >= 0.3.1b)

eiogeteventstream - Повертає потік, що відображає змінну, що використовується при взаємодії з libeio

### Опис

```methodsynopsis
eio_get_event_stream(): mixed
```

**eiogeteventstream()** отримує потік, що відображає змінну, що використовується при взаємодії з libeio. Може бути використане для прив'язки деякого циклу обробки, що поставляється іншим модулем PECL, наприклад libevent.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**eiogeteventstream()** повертає потік у разі успішного виконання або **`null`** у разі виникнення помилки.

### Приклади

**Приклад #1 Використання eio спільно з libevent**

```php
<?php
function my_eio_poll($fd, $events, $arg) {
    /* Некоторые действия с libevent могут быть здесь */
    if (eio_nreqs()) {
        eio_poll();
    }
    /* .. и здесь */
}

function my_res_cb($d, $r) {
    var_dump($r); var_dump($d);
}

$base = event_base_new();
$event = event_new();

$fd = eio_get_event_stream();
var_dump($fd);

eio_nop(EIO_PRI_DEFAULT, "my_res_cb", "nop data");
eio_mkdir("/tmp/abc-eio-temp", 0750, EIO_PRI_DEFAULT, "my_res_cb", "mkdir data");
/* Прочие eio_* запросы  ... */


// Установка флагов события
event_set($event, $fd, EV_READ /*| EV_PERSIST*/, "my_eio_poll", array($event, $base));

// Установка основы события
event_base_set($event, $base);

// Включение события
event_add($event);

// Запуск цикла обработки
event_base_loop($base);

/* То же самое доступно через интерфейс буфера libevent */
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
int(0)
string(8) "nop data"
int(0)
string(10) "mkdir data"
```