---
navigation:
  - swoole-coroutine.suspend.md: '« SwooleCoroutine::suspend'
  - swoole-event.add.md: 'SwooleEvent::add »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleEvent
---
# Клас SwooleEvent

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Event
     
     {


    /* Методы */
    
   public static add(    int $fd,    callable $read_callback,    callable $write_callback = ?,    string $events = ?): bool
public static defer(mixed $callback): void
public static del(string $fd): bool
public static exit(): void
public static set(    int $fd,    string $read_callback = ?,    string $write_callback = ?,    string $events = ?): bool
public static wait(): void
public static write(string $fd, string $data): void

   }
```

## Зміст

-   [SwooleEvent::add](swoole-event.add.md) — Додає нові callback функції сокету в EventLoop
-   [SwooleEvent::defer](swoole-event.defer.md) — Додає callback-функцію до наступного циклу подій
-   [SwooleEvent::del](swoole-event.del.md) - Видаляє всі callback-функції події сокету
-   [SwooleEvent::exit](swoole-event.exit.md) — Виходить із циклу подій, доступно лише на стороні клієнта
-   [SwooleEvent::set](swoole-event.set.md) - Оновлює callback-функції події сокету
-   [SwooleEvent::wait](swoole-event.wait.md) - Опис
-   [SwooleEvent::write](swoole-event.write.md) - Записує дані в сокет
