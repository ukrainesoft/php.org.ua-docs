---
navigation:
  - ev.depth.md: '« Ev::depth'
  - ev.feedsignal.md: 'Ev::feedSignal »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::embeddableBackends'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::embeddableBackends

(PECL ev >= 0.2.0)

Ev::embeddableBackends — Повертає набір бекендів, які можна вбудувати в інші цикли подій

### Опис

```methodsynopsis
final
   public
   static
   Ev::embeddableBackends(): int
```

Повертає набір бекендів, які можна вбудувати в інші цикли подій.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає бітову маску, що містить [прапори бекенда](class.ev.md#ev.constants.watcher-backends), об'єднані за допомогою побітового *АБО*

### Приклади

**Приклад #1 Цикл створюється за допомогою kqueue і вбудовується в цикл за замовчуванням**

```php
<?php
/*
* Проверяем, что kqueue доступен, но не рекомендован и создаём kqueue бэкенд
* с использованием сокетов (которые обычно работают с любой реализацией kqueue).
* Сохраняем событийный цикл kqueue/socket-only в loop_socket. (Можем, опционально
* использовать флаг EVFLAG_NOENV)
*
* Приклад взят с сайта
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
 if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
  $embed = new EvEmbed($loop);
 }
}

if (!$socket_loop) {
 $socket_loop = $loop;
}

// Теперь используем $socket_loop для всех сокетов и $loop всего остального
?>
```

### Дивіться також

-   [EvEmbed](class.evembed.md)
-   [Ev::recommendedBackends()](ev.recommendedbackends.md) \- Отримати бітову маску рекомендованих бекендів для даної платформи
-   [Ev::supportedBackends()](ev.supportedbackends.md) \- Повертає набір бекендів, які підтримуються поточною конфігурацією libev
-   [Прапори бекенда](class.ev.md#ev.constants.watcher-backends)
-   [Приклади](ev.examples.md)
