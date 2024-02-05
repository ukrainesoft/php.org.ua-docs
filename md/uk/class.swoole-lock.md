---
navigation:
  - swoole-http-server.start.md: '« Swoole\\Http\\Server::start'
  - swoole-lock.construct.md: 'Swoole\\Lock::\_\_construct »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Lock
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Lock

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Lock
     
     {


    /* Методы */
    
   public __destruct(): void
public lock_read(): void
public lock(): void
public trylock_read(): void
public trylock(): void
public unlock(): void

   }
```

## Зміст

-   [Swoole\\Lock::\_\_construct](swoole-lock.construct.md)— Створює блокування пам'яті
-   [Swoole\\Lock::\_\_destruct](swoole-lock.destruct.md)— Знищує блокування пам'яті Swoole
-   [Swoole\\Lock::lock\_read](swoole-lock.lock-read.md)— Блокує читання-запис блокування для читання
-   [Swoole\\Lock::lock](swoole-lock.lock.md)— Намагається отримати блокування. Заблокується, якщо блокування недоступне
-   [Swoole\\Lock::trylock\_read](swoole-lock.trylock-read.md)— Намагається заблокувати блокування читання-запису для читання і відразу повертає, навіть якщо блокування недоступне
-   [Swoole\\Lock::trylock](swoole-lock.trylock.md)— Намагається отримати блокування і відразу повертає, навіть якщо блокування недоступне
-   [Swoole\\Lock::unlock](swoole-lock.unlock.md) \- Знімає блокування
