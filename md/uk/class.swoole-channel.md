Клас SwooleChannel

-   [« SwooleBuffer::write](swoole-buffer.write.html)
    
-   [SwooleChannel::construct »](swoole-channel.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleChannel
    

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

-   [SwooleChannel::construct](swoole-channel.construct.html) - Створює канал Swoole
-   [SwooleChannel::destruct](swoole-channel.destruct.html) - Знищує канал Swoole
-   [SwooleChannel::pop](swoole-channel.pop.html) — Читає та витягує дані з каналу Swoole
-   [SwooleChannel::push](swoole-channel.push.html) — Записує та передає дані до каналу Swoole
-   [SwooleChannel::stats](swoole-channel.stats.html) — Отримує статистику каналу Swoole