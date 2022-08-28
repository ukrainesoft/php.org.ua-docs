Отримати інформацію про addrinfo

-   [« socket\_addrinfo\_connect](function.socket-addrinfo-connect.html)
    
-   [socket\_addrinfo\_lookup »](function.socket-addrinfo-lookup.html)
    
-   [PHP Manual](index.html)
    
-   [Функции сокета](ref.sockets.html)
    
-   Отримати інформацію про addrinfo
    

# socketaddrinfoexplain

(PHP 7> = 7.2.0, PHP 8)

socketaddrinfoexplain — Отримати інформацію про addrinfo

### Опис

```methodsynopsis
socket_addrinfo_explain(AddressInfo $address): array
```

Функція **socketaddrinfoexplain()** надає доступ до базової структури `addrinfo`

### Список параметрів

`address`

Екземпляр [AddressInfo](class.addressinfo.html), створений за допомогою [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html)

### Значення, що повертаються

Повертає масив, що містить поля у структурі `addrinfo`

### список змін

| Версия | Описание |
| --- | --- |
|  | `address` тепер екземпляр класу [AddressInfo](class.addressinfo.html); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.html) - Створити та прив'язати до сокету із вказаного addrinfo
-   [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.html) - Створити та підключитися до сокету із зазначеного addrinfo
-   [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.html) - Отримати масив з вмістом getaddrinfo про вказане ім'я хоста