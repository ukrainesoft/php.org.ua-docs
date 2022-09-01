---
navigation:
  - class.evembed.html: « EvEmbed
  - evembed.createstopped.html: 'EvEmbed::createStopped »'
  - index.html: PHP Manual
  - class.evembed.html: EvEmbed
title: 'EvEmbed::construct'
---
# EvEmbed::construct

(PECL ev >= 0.2.0)

EvEmbed::construct — Конструктор об'єкту EvEmbed

### Опис

public **EvEmbed::construct**  
object `$other`  
[callable](language.types.callable.html) `$callback`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data`  
int `$priority`

Це досить просунутий тип спостерігача, який дозволяє вбудувати один цикл подій в інший (нині підтримуються лише події введення-виводу у вбудованому циклі, інші типи спостерігачів можуть оброблятися із затримкою чи неправильно і не повинні використовуватися).

Детальніше читайте в [» документации libev](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#code_ev_embed_code_when_one_backend_)

Цей спостерігач найбільш корисний у *BSD* системах без працюючого `kqueue` для підтримки обробки великої кількості сокетів. Дивіться приклад нижче.

### Список параметрів

`other`

Екземпляр класу [EvLoop](class.evloop.html). Подієвий цикл для вбудовування. Цей цикл має бути вбудованим (дивіться [Ev::embeddableBackends()](ev.embeddablebackends.html)

`callback`

Дивіться [callback-функції спостерігачів](ev.watcher-callbacks.html)

`data`

Дані користувача, асоційовані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Приклади

**Приклад #1 Вбудовування циклу, створеного за допомогою kqueue у циклі подій за умовчанням**

```php
<?php
/*
 * Проверьте, доступен ли kqueue и создайте бэкенд kqueue
 * для использования с сокетами (это обычно работает с любой реализацией kqueue).
 * Сохраните событийный цикл kqueue/socket-only в loop_socket. (Опционально можно
 * использовать флаг EVFLAG_NOENV)
 *
 * пример взят из
 * http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
 */
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
    if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
        $embed = new EvEmbed($loop);
    }
}

if (!$socket_loop) {
    $socket_loop = $loop;
}

// теперь используйте $socket_loop для всех сокетов, а $loop для всего остального
?>
```

### Дивіться також

-   [Ev::embeddableBackends()](ev.embeddablebackends.html) - Повертає набір бекендів, які можна вбудувати в інші цикли подій
