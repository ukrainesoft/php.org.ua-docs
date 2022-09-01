---
navigation:
  - evwatcher.invoke.md: '« EvWatcher::invoke'
  - evwatcher.setcallback.md: 'EvWatcher::setCallback »'
  - index.md: PHP Manual
  - class.evwatcher.md: EvWatcher
title: 'EvWatcher::keepalive'
---
# EvWatcher::keepalive

(PECL ev >= 0.2.0)

EvWatcher::keepalive — Налаштовує, чи повертатиметься цикл

### Опис

```methodsynopsis
public
   EvWatcher::keepalive(
    bool
     $value
    = ?): bool
```

Налаштовує, чи повертатиметься цикл. Якщо `value` підтримки встановлено **`false`**, спостерігач не перешкоджатиме поверненню [Ev::run()](ev.run.md) [EvLoop::run()](evloop.run.md)навіть якщо спостерігач активний.

Спостерігачі за замовчуванням мають `value` підтримки **`true`**

Очищення статусу підтримки корисне при поверненні з [Ev::run()](ev.run.md) [EvLoop::run()](evloop.run.md) лише тому, що спостерігач небажаний. Це може бути працюючий спостерігач UDP-сокету або близько того.

### Список параметрів

`value`

Якщо `value` підтримки встановлено **`false`**, спостерігач не перешкоджатиме поверненню [Ev::run()](ev.run.md) [EvLoop::run()](evloop.run.md)навіть якщо спостерігач активний.

### Значення, що повертаються

Повертає попередній стан.

### Приклади

**Приклад #1 Реєструємо спостерігач вводу-виводу для будь-якого UDP-сокету, але не перешкоджаємо запуску циклу подій тільки через цей спостерігач.**

```php
<?php
$udp_socket = ...
$udp_watcher = new EvIo($udp_socket, Ev::READ, function () { /* ... */ });
$udp_watcher->keepalive(FALSE);
?>
```
