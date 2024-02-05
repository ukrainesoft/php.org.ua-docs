---
navigation:
  - yar-client.setopt.md: '« Yar\_Client::setOpt'
  - yar-concurrent-client.call.md: 'Yar\_Concurrent\_Client::call »'
  - index.md: PHP Manual
  - book.yar.md: Yar
title: Клас Yar\_Concurrent\_Client
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yar\_Concurrent\_Client

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

\_callstack

\_callback

\_error\_callback

## Зміст

-   [Yar\_Concurrent\_Client::call](yar-concurrent-client.call.md)— Зареєструвати конкурентний виклик
-   [Yar\_Concurrent\_Client::loop](yar-concurrent-client.loop.md)— Запуск усіх зареєстрованих викликів
-   [Yar\_Concurrent\_Client::reset](yar-concurrent-client.reset.md)— Очистити всі зареєстровані дзвінки
