---
navigation:
  - swoole-http-server.start.md: '« SwooleHttpServer::start'
  - swoole-lock.construct.md: 'SwooleLock::construct »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleLock
---
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

-   [SwooleLock::construct](swoole-lock.construct.md) — Створює блокування пам'яті
-   [SwooleLock::destruct](swoole-lock.destruct.md) — Знищує блокування пам'яті Swoole
-   [SwooleLock::lockread](swoole-lock.lock-read.md) — Блокує читання-запис блокування для читання
-   [SwooleLock::lock](swoole-lock.lock.md) — Намагається отримати блокування. Заблокується, якщо блокування недоступне
-   [SwooleLock::trylockread](swoole-lock.trylock-read.md) — Намагається заблокувати блокування читання-запису для читання і відразу повертає, навіть якщо блокування недоступне
-   [SwooleLock::trylock](swoole-lock.trylock.md) — Намагається отримати блокування і відразу повертає, навіть якщо блокування недоступне
-   [SwooleLock::unlock](swoole-lock.unlock.md) - Знімає блокування
