Отримати останню помилку сокету, що виникла

-   [« EventUtil::getLastSocketErrno](eventutil.getlastsocketerrno.html)
    
-   [EventUtil::getSocketFd »](eventutil.getsocketfd.html)
    
-   [PHP Manual](index.html)
    
-   [EventUtil](class.eventutil.html)
    
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

-   [EventUtil::getLastSocketErrno()](eventutil.getlastsocketerrno.html) - Отримати номер останньої помилки сокету, що виникла