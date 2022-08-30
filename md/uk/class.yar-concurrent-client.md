Клас YarConcurrentClient

-   [« YarClient::setOpt](yar-client.setopt.html)
    
-   [YarConcurrentClient::call »](yar-concurrent-client.call.html)
    
-   [PHP Manual](index.html)
    
-   [Yar](book.yar.html)
    
-   Клас YarConcurrentClient
    

# Клас YarConcurrentClient

(No version information available, might only be in Git)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Yar_Concurrent_Client
     
     {
    
    /* Свойства */
    
     static
      $_callstack;

    static
      $_callback;

    static
      $_error_callback;



    /* Методы */
    
   public static call(    string $uri,    string $method,    array $parameters = ?,    callable $callback = ?,    callable $error_callback = ?,    array $options = ?): int
public static loop(callable $callback = ?, callable $error_callback = ?): bool
public static reset(): bool

   }
```

## Властивості

callstack

callback

errorcallback

## Зміст

-   [YarConcurrentClient::call](yar-concurrent-client.call.html) — Зареєструвати конкурентний виклик
-   [YarConcurrentClient::loop](yar-concurrent-client.loop.html) — Запуск усіх зареєстрованих викликів
-   [YarConcurrentClient::reset](yar-concurrent-client.reset.html) — Очистити всі зареєстровані дзвінки