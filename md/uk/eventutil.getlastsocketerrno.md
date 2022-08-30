Отримати номер останньої помилки сокету, що виникла

-   [« EventUtil::construct](eventutil.construct.md)
    
-   [EventUtil::getLastSocketError »](eventutil.getlastsocketerror.md)
    
-   [PHP Manual](index.md)
    
-   [EventUtil](class.eventutil.md)
    
-   Отримати номер останньої помилки сокету, що виникла
    

# EventUtil::getLastSocketErrno

(PECL event >= 1.2.6-beta)

EventUtil::getLastSocketErrno — Отримати номер останньої помилки сокету, що виникла

### Опис

```methodsynopsis
public
   static
   EventUtil::getLastSocketErrno(
    mixed
     $socket
     = null
   ): int
```

Повертає номер останньої помилки сокету ( `errno`

### Список параметрів

`socket`

Ресурс сокету, потоку чи файловий дескриптор сокету.

### Значення, що повертаються

Повертає номер останньої помилки сокету ( `errno`

### Дивіться також

-   [EventUtil::getLastSocketError()](eventutil.getlastsocketerror.md) - Отримати останню помилку сокету, що виникла