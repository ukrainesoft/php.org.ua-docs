Клас SwooleAtomic

-   [« SwooleAsync::writeFile](swoole-async.writefile.html)
    
-   [SwooleAtomic::add »](swoole-atomic.add.html)
    
-   [PHP Manual](index.md)
    
-   [Swoole](book.swoole.md)
    
-   Клас SwooleAtomic
    

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

-   [SwooleAtomic::add](swoole-atomic.add.html) - Додає число до значення атомарного об'єкта
-   [SwooleAtomic::cmpset](swoole-atomic.cmpset.html) — Порівнює та встановлює значення атомарного об'єкта
-   [SwooleAtomic::construct](swoole-atomic.construct.html) - Створює атомарний об'єкт swoole
-   [SwooleAtomic::get](swoole-atomic.get.html) — Отримує поточне значення атомарного об'єкта
-   [SwooleAtomic::set](swoole-atomic.set.html) — Встановлює нове значення для атомарного об'єкту
-   [SwooleAtomic::sub](swoole-atomic.sub.html) — Віднімає число із значення атомарного об'єкта