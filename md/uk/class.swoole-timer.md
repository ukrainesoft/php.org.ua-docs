Клас SwooleTimer

-   [« Swoole\\Table::valid](swoole-table.valid.html)
    
-   [Swoole\\Timer::after »](swoole-timer.after.html)
    
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

-   [Swoole\\Timer::after](swoole-timer.after.html) - Запускає callback-функцію через певний проміжок часу
-   [Swoole\\Timer::clear](swoole-timer.clear.html) — Видаляє таймер за ідентифікатором
-   [Swoole\\Timer::exists](swoole-timer.exists.html) — Перевіряє, чи існує таймер
-   [Swoole\\Timer::tick](swoole-timer.tick.html) — Повторює цю функцію у кожний заданий інтервал часу