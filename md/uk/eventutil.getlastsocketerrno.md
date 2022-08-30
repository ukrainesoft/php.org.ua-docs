Отримати номер останньої помилки сокету, що виникла

-   [« EventUtil::construct](eventutil.construct.html)
    
-   [EventUtil::getLastSocketError »](eventutil.getlastsocketerror.html)
    
-   [PHP Manual](index.html)
    
-   [EventUtil](class.eventutil.html)
    
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

-   [EventUtil::getLastSocketError()](eventutil.getlastsocketerror.html) - Отримати останню помилку сокету, що виникла