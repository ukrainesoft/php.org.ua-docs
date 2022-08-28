Повертає версію шифру, який використовується поточним SSL-з'єднанням

-   [« EventBufferEvent::sslGetCipherName](eventbufferevent.sslgetciphername.html)
    
-   [EventBufferEvent::sslGetProtocol »](eventbufferevent.sslgetprotocol.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
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