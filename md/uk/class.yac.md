Клас Yac

-   [« Обумовлені константи](yac.constants.md)
    
-   [Yac::add »](yac.add.md)
    
-   [PHP Manual](index.md)
    
-   [Yac](book.yac.md)
    
-   Клас Yac
    

# Клас Yac

(PECL yac >= 1.0.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Yac
     
     {

    /* Свойства */
    
     protected
      $_prefix;



    /* Методы */
    
   public __construct(string $prefix = "")

    public add(string $keys, mixed $value, int $ttl = 0): bool
public add(array $key_vals): bool
public delete(string|array $keys, int $ttl = ?): bool
public dump(int $$num): mixed
public flush(): bool
public get(string|array $key, int &$cas = null): mixed
public __get(string $key): mixed
public info(): array
public set(string $keys, mixed $value, int $ttl = 0): bool
public add(array $key_vals): bool
public __set(string $keys, mixed $value): mixed

   }
```

## Властивості

prefix

## Зміст

-   [Yac::add](yac.add.md) - Зберігає в кеш
-   [Yac::construct](yac.construct.md) - Конструктор класу
-   [Yac::delete](yac.delete.md) — Видаляє елементи з кешу
-   [Yac::dump](yac.dump.md) - Дамп кеша
-   [Yac::flush](yac.flush.md) - Очищає кеш
-   [Yac::get](yac.get.md) — Витягує значення з кешу
-   [Yac::get](yac.getter.md) - Геттер
-   [Yac::info](yac.info.md) - Стан кешу
-   [Yac::set](yac.set.md) - Зберігає в кеш
-   [Yac::set](yac.setter.md) - Сеттер