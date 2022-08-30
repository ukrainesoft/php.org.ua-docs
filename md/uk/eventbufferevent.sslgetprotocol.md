Повертає ім'я протоколу, який використовується для поточного з'єднання SSL

-   [« EventBufferEvent::sslGetCipherVersion](eventbufferevent.sslgetcipherversion.md)
    
-   [EventBufferEvent::sslRenegotiate »](eventbufferevent.sslrenegotiate.md)
    
-   [PHP Manual](index.md)
    
-   [EventBufferEvent](class.eventbufferevent.md)
    
-   Повертає ім'я протоколу, який використовується для поточного з'єднання SSL
    

# EventBufferEvent::sslGetProtocol

(PECL event >= 1.10.0)

EventBufferEvent::sslGetProtocol — Повертає ім'я протоколу, який використовується для поточного з'єднання SSL

### Опис

```methodsynopsis
public
   EventBufferEvent::sslGetProtocol(): string
```

Повертає ім'я протоколу, який використовується для поточного з'єднання SSL.

> **Зауваження**
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я протоколу, який використовується для поточного з'єднання SSL.