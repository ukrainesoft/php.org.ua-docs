Клас SwooleLock

-   [« Swoole\\Http\\Server::start](swoole-http-server.start.html)
    
-   [Swoole\\Lock::\_\_construct »](swoole-lock.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleLock
    

# Клас SwooleLock

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

-   [Swoole\\Lock::\_\_construct](swoole-lock.construct.html) — Створює блокування пам'яті
-   [Swoole\\Lock::\_\_destruct](swoole-lock.destruct.html) — Знищує блокування пам'яті Swoole
-   [Swoole\\Lock::lock\_read](swoole-lock.lock-read.html) — Блокує читання-запис блокування для читання
-   [Swoole\\Lock::lock](swoole-lock.lock.html) — Намагається отримати блокування. Заблокується, якщо блокування недоступне
-   [Swoole\\Lock::trylock\_read](swoole-lock.trylock-read.html) — Намагається заблокувати блокування читання-запису для читання і відразу повертає, навіть якщо блокування недоступне
-   [Swoole\\Lock::trylock](swoole-lock.trylock.html) — Намагається отримати блокування і відразу повертає, навіть якщо блокування недоступне
-   [Swoole\\Lock::unlock](swoole-lock.unlock.html) - Знімає блокування