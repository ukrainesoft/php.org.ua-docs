---
navigation:
  - swoole-coroutine.suspend.md: '« Swoole\\Coroutine::suspend'
  - swoole-event.add.md: 'Swoole\\Event::add »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Event
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Event

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

-   [Swoole\\Event::add](swoole-event.add.md)— Додає нові callback функції сокету в EventLoop
-   [Swoole\\Event::defer](swoole-event.defer.md)— Додає callback-функцію до наступного циклу подій
-   [Swoole\\Event::del](swoole-event.del.md) \- Видаляє всі callback-функції події сокету
-   [Swoole\\Event::exit](swoole-event.exit.md)— Виходить із циклу подій, доступно лише на стороні клієнта
-   [Swoole\\Event::set](swoole-event.set.md) \- Оновлює callback-функції події сокету
-   [Swoole\\Event::wait](swoole-event.wait.md) \- Опис
-   [Swoole\\Event::write](swoole-event.write.md) \- Записує дані в сокет
