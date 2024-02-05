---
navigation:
  - swoole-async.writefile.md: '« Swoole\\Async::writeFile'
  - swoole-atomic.add.md: 'Swoole\\Atomic::add »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Atomic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Atomic

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

-   [Swoole\\Atomic::add](swoole-atomic.add.md) \- Додає число до значення атомарного об'єкта
-   [Swoole\\Atomic::cmpset](swoole-atomic.cmpset.md)— Порівнює та встановлює значення атомарного об'єкта
-   [Swoole\\Atomic::\_\_construct](swoole-atomic.construct.md) \- Створює атомарний об'єкт swoole
-   [Swoole\\Atomic::get](swoole-atomic.get.md)— Отримує поточне значення атомарного об'єкта
-   [Swoole\\Atomic::set](swoole-atomic.set.md)— Встановлює нове значення для атомарного об'єкту
-   [Swoole\\Atomic::sub](swoole-atomic.sub.md)— Віднімає число із значення атомарного об'єкта
