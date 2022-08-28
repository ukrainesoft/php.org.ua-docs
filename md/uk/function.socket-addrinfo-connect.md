Створити та підключитися до сокету із вказаного addrinfo

-   [« socket\_addrinfo\_bind](function.socket-addrinfo-bind.html)
    
-   [socket\_addrinfo\_explain »](function.socket-addrinfo-explain.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Створити та підключитися до сокету із вказаного addrinfo
    

# socketaddrinfoconnect

(PHP 7> = 7.2.0, PHP 8)

socketaddrinfoconnect — Створити та підключитися до сокету із вказаного addrinfo

### Опис

```methodsynopsis
socket_addrinfo_connect(AddressInfo $address): Socket|false
```

Створити екземпляр [Socket](class.socket.html) та підключити його до наданого екземпляра [AddressInfo](class.addressinfo.html). Значення цієї функції, що повертається, може використовуватися з іншими функціями сокету.

### Список параметрів

`address`

Екземпляр [AddressInfo](class.addressinfo.html), створений за допомогою [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html)

### Значення, що повертаються

Повертає екземпляр [Socket](class.socket.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.html); раніше повертався ресурс (resource). |
|  | `address` тепер екземпляр класу [AddressInfo](class.addressinfo.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.html) - Створити та прив'язати до сокету із вказаного addrinfo
-   [socket\_addrinfo\_explain()](function.socket-addrinfo-explain.html) - Отримати інформацію про addrinfo
-   [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html) - Отримати масив з вмістом getaddrinfo про вказане ім'я хоста