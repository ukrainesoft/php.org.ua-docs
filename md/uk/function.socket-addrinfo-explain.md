---
navigation:
  - function.socket-addrinfo-connect.html: « socketaddrinfoconnect
  - function.socket-addrinfo-lookup.html: socketaddrinfolookup »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketaddrinfoexplain
---
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

Екземпляр [AddressInfo](class.addressinfo.md), створений за допомогою [socketaddrinfolookup()](function.socket-addrinfo-lookup.md)

### Значення, що повертаються

Повертає масив, що містить поля у структурі `addrinfo`

### список змін

| Версия | Описание |
| --- | --- |
|  | `address` тепер екземпляр класу [AddressInfo](class.addressinfo.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketaddrinfobind()](function.socket-addrinfo-bind.md) - Створити та прив'язати до сокету із вказаного addrinfo
-   [socketaddrinfoconnect()](function.socket-addrinfo-connect.md) - Створити та підключитися до сокету із зазначеного addrinfo
-   [socketaddrinfolookup()](function.socket-addrinfo-lookup.md) - Отримати масив з вмістом getaddrinfo про вказане ім'я хоста
