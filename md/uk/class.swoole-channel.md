---
navigation:
  - swoole-buffer.write.md: '« Swoole\\Buffer::write'
  - swoole-channel.construct.md: 'Swoole\\Channel::\_\_construct »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Channel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Channel

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Channel
     
     {


    /* Методы */
    
   public __destruct(): void
public pop(): mixed
public push(string $data): bool
public stats(): array

   }
```

## Зміст

-   [Swoole\\Channel::\_\_construct](swoole-channel.construct.md) \- Створює канал Swoole
-   [Swoole\\Channel::\_\_destruct](swoole-channel.destruct.md) \- Знищує канал Swoole
-   [Swoole\\Channel::pop](swoole-channel.pop.md)— Читає та витягує дані з каналу Swoole
-   [Swoole\\Channel::push](swoole-channel.push.md)— Записує та передає дані до каналу Swoole
-   [Swoole\\Channel::stats](swoole-channel.stats.md)— Отримує статистику каналу Swoole
