---
navigation:
  - swoole-async.writefile.html: '« SwooleAsync::writeFile'
  - swoole-atomic.add.html: 'SwooleAtomic::add »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleAtomic
---
# Клас SwooleAtomic

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Atomic
     
     {


    /* Методы */
    
   public add(int $add_value = ?): int
public cmpset(int $cmp_value, int $new_value): int
public get(): int
public set(int $value): int
public sub(int $sub_value = ?): int

   }
```

## Зміст

-   [SwooleAtomic::add](swoole-atomic.add.md) - Додає число до значення атомарного об'єкта
-   [SwooleAtomic::cmpset](swoole-atomic.cmpset.md) — Порівнює та встановлює значення атомарного об'єкта
-   [SwooleAtomic::construct](swoole-atomic.construct.md) - Створює атомарний об'єкт swoole
-   [SwooleAtomic::get](swoole-atomic.get.md) — Отримує поточне значення атомарного об'єкта
-   [SwooleAtomic::set](swoole-atomic.set.md) — Встановлює нове значення для атомарного об'єкту
-   [SwooleAtomic::sub](swoole-atomic.sub.md) — Віднімає число із значення атомарного об'єкта
