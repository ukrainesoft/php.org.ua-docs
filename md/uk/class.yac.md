Клас Yac

-   [« Предопределённые константы](yac.constants.html)
    
-   [Yac::add »](yac.add.html)
    
-   [PHP Manual](index.html)
    
-   [Yac](book.yac.html)
    
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

-   [Yac::add](yac.add.html) - Зберігає в кеш
-   [Yac::construct](yac.construct.html) - Конструктор класу
-   [Yac::delete](yac.delete.html) — Видаляє елементи з кешу
-   [Yac::dump](yac.dump.html) - Дамп кеша
-   [Yac::flush](yac.flush.html) - Очищає кеш
-   [Yac::get](yac.get.html) — Витягує значення з кешу
-   [Yac::get](yac.getter.html) - Геттер
-   [Yac::info](yac.info.html) - Стан кешу
-   [Yac::set](yac.set.html) - Зберігає в кеш
-   [Yac::set](yac.setter.html) - Сеттер