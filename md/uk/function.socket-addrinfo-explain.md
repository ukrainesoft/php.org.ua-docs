---
navigation:
  - function.socket-addrinfo-connect.md: « socket\_addrinfo\_connect
  - function.socket-addrinfo-lookup.md: socket\_addrinfo\_lookup »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_addrinfo\_explain
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_addrinfo\_explain

(PHP 7 >= 7.2.0, PHP 8)

socket\_addrinfo\_explain — Отримати інформацію про addrinfo

### Опис

```methodsynopsis
socket_addrinfo_explain(AddressInfo $address): array
```

Функция\*\*socket\_addrinfo\_explain()\*\*предоставляет доступ к базовой структуре`addrinfo`

### Список параметрів

`address`

Екземпляр [AddressInfo](class.addressinfo.md), створений за допомогою [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.md)

### Значення, що повертаються

Повертає масив, що містить поля у структурі `addrinfo`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `address` тепер екземпляр класу [AddressInfo](class.addressinfo.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.md) \- Створити та прив'язати до сокету із зазначеного addrinfo
-   [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.md) \- Створити та підключитися до сокету із зазначеного addrinfo
-   [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.md) \- Отримати масив з вмістом getaddrinfo про вказане ім'я хоста
