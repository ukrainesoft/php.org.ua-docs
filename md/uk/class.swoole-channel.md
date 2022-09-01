---
navigation:
  - swoole-buffer.write.html: '« SwooleBuffer::write'
  - swoole-channel.construct.html: 'SwooleChannel::construct »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleChannel
---
# Клас SwooleChannel

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

-   [SwooleChannel::construct](swoole-channel.construct.md) - Створює канал Swoole
-   [SwooleChannel::destruct](swoole-channel.destruct.md) - Знищує канал Swoole
-   [SwooleChannel::pop](swoole-channel.pop.md) — Читає та витягує дані з каналу Swoole
-   [SwooleChannel::push](swoole-channel.push.md) — Записує та передає дані до каналу Swoole
-   [SwooleChannel::stats](swoole-channel.stats.md) — Отримує статистику каналу Swoole
