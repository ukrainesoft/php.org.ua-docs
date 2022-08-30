Повертає версію шифру, який використовується поточним SSL-з'єднанням

-   [« EventBufferEvent::sslGetCipherName](eventbufferevent.sslgetciphername.md)
    
-   [EventBufferEvent::sslGetProtocol »](eventbufferevent.sslgetprotocol.md)
    
-   [PHP Manual](index.md)
    
-   [EventBufferEvent](class.eventbufferevent.md)
    
-   Повертає версію шифру, який використовується поточним SSL-з'єднанням
    

# EventBufferEvent::sslGetCipherVersion

(PECL event >= 1.10.0)

EventBufferEvent::sslGetCipherVersion — Повертає версію шифру, що використовується поточним SSL-з'єднанням

### Опис

```methodsynopsis
public
   EventBufferEvent::sslGetCipherVersion(): string
```

Отримує версію шифру, який використовується поточним з'єднанням SSL.

> **Зауваження**
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточну версію шифрованого з'єднання SSL або **`false`** у разі виникнення помилки.