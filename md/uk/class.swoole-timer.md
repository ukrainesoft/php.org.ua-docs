Клас SwooleTimer

-   [« SwooleTable::valid](swoole-table.valid.html)
    
-   [SwooleTimer::after »](swoole-timer.after.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleTimer
    

# Клас SwooleTimer

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Timer
     
     {


    /* Методы */
    
            public static after(int $after_time_ms, callable $callback): void
public static clear(int $timer_id): void
public static exists(int $timer_id): bool
public static tick(int $interval_ms, callable $callback, string $param = ?): void

   }
```

## Зміст

-   [SwooleTimer::after](swoole-timer.after.html) - Запускає callback-функцію через певний проміжок часу
-   [SwooleTimer::clear](swoole-timer.clear.html) — Видаляє таймер за ідентифікатором
-   [SwooleTimer::exists](swoole-timer.exists.html) — Перевіряє, чи існує таймер
-   [SwooleTimer::tick](swoole-timer.tick.html) — Повторює цю функцію у кожний заданий інтервал часу