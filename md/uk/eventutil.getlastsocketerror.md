Отримати останню помилку сокету, що виникла

-   [« EventUtil::getLastSocketErrno](eventutil.getlastsocketerrno.md)
    
-   [EventUtil::getSocketFd »](eventutil.getsocketfd.md)
    
-   [PHP Manual](index.md)
    
-   [EventUtil](class.eventutil.md)
    
-   Отримати останню помилку сокету, що виникла
    

# EventUtil::getLastSocketError

(PECL event >= 1.2.6-beta)

EventUtil::getLastSocketError — Отримати останню помилку сокету, що виникла.

### Опис

```methodsynopsis
public
   static
   EventUtil::getLastSocketError(
    mixed
     $socket
    = ?): string
```

Повертає останню помилку сокету, що виникла.

### Список параметрів

`socket`

Ресурс сокету, потоку чи файловий дескриптор сокету.

### Значення, що повертаються

Повертає останню помилку сокету, що виникла.

### Дивіться також

-   [EventUtil::getLastSocketErrno()](eventutil.getlastsocketerrno.md) - Отримати номер останньої помилки сокету, що виникла