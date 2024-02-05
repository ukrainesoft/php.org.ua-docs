---
navigation:
  - swoole-table.valid.md: '« Swoole\\Table::valid'
  - swoole-timer.after.md: 'Swoole\\Timer::after »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Timer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Timer

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

-   [Swoole\\Timer::after](swoole-timer.after.md) \- Запускає callback-функцію через певний проміжок часу
-   [Swoole\\Timer::clear](swoole-timer.clear.md)— Видаляє таймер за ідентифікатором
-   [Swoole\\Timer::exists](swoole-timer.exists.md)— Перевіряє, чи існує таймер
-   [Swoole\\Timer::tick](swoole-timer.tick.md)— Повторює цю функцію у кожний заданий інтервал часу
