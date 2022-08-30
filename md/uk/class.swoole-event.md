Клас SwooleEvent

-   [« SwooleCoroutine::suspend](swoole-coroutine.suspend.html)
    
-   [SwooleEvent::add »](swoole-event.add.html)
    
-   [PHP Manual](index.md)
    
-   [Swoole](book.swoole.md)
    
-   Клас SwooleEvent
    

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

-   [SwooleEvent::add](swoole-event.add.html) — Додає нові callback функції сокету в EventLoop
-   [SwooleEvent::defer](swoole-event.defer.html) — Додає callback-функцію до наступного циклу подій
-   [SwooleEvent::del](swoole-event.del.html) - Видаляє всі callback-функції події сокету
-   [SwooleEvent::exit](swoole-event.exit.html) — Виходить із циклу подій, доступно лише на стороні клієнта
-   [SwooleEvent::set](swoole-event.set.html) - Оновлює callback-функції події сокету
-   [SwooleEvent::wait](swoole-event.wait.html) - Опис
-   [SwooleEvent::write](swoole-event.write.html) - Записує дані в сокет