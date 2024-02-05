---
navigation:
  - yac.constants.md: « Зумовлені константи
  - yac.add.md: 'Yac::add »'
  - index.md: PHP Manual
  - book.yac.md: Yac
title: Клас Yac
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

\_prefix

## Зміст

-   [Yac::add](yac.add.md) \- Зберігає в кеш
-   [Yac::\_\_construct](yac.construct.md) \- Конструктор класу
-   [Yac::delete](yac.delete.md)— Видаляє елементи з кешу
-   [Yac::dump](yac.dump.md) \- Дамп кеша
-   [Yac::flush](yac.flush.md) \- Очищає кеш
-   [Yac::get](yac.get.md)— Витягує значення з кешу
-   [Yac::\_\_get](yac.getter.md) \- Геттер
-   [Yac::info](yac.info.md) \- Стан кешу
-   [Yac::set](yac.set.md) \- Зберігає в кеш
-   [Yac::\_\_set](yac.setter.md) \- Сеттер
