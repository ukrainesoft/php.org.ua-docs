Клас SwooleLock

-   [« SwooleHttpServer::start](swoole-http-server.start.html)
    
-   [SwooleLock::construct »](swoole-lock.construct.html)
    
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

-   [SwooleLock::construct](swoole-lock.construct.html) — Створює блокування пам'яті
-   [SwooleLock::destruct](swoole-lock.destruct.html) — Знищує блокування пам'яті Swoole
-   [SwooleLock::lockread](swoole-lock.lock-read.html) — Блокує читання-запис блокування для читання
-   [SwooleLock::lock](swoole-lock.lock.html) — Намагається отримати блокування. Заблокується, якщо блокування недоступне
-   [SwooleLock::trylockread](swoole-lock.trylock-read.html) — Намагається заблокувати блокування читання-запису для читання і відразу повертає, навіть якщо блокування недоступне
-   [SwooleLock::trylock](swoole-lock.trylock.html) — Намагається отримати блокування і відразу повертає, навіть якщо блокування недоступне
-   [SwooleLock::unlock](swoole-lock.unlock.html) - Знімає блокування