---
navigation:
  - function.socket-addrinfo-bind.md: « socketaddrinfobind
  - function.socket-addrinfo-explain.md: socketaddrinfoexplain »
  - index.md: PHP Manual
  - ref.sockets.md: Функции сокета
title: socketaddrinfoconnect
---
# socketaddrinfoconnect

(PHP 7> = 7.2.0, PHP 8)

socketaddrinfoconnect — Створити та підключитися до сокету із вказаного addrinfo

### Опис

```methodsynopsis
socket_addrinfo_connect(AddressInfo $address): Socket|false
```

Створити екземпляр [Socket](class.socket.md) та підключити його до наданого екземпляра [AddressInfo](class.addressinfo.md). Значення цієї функції, що повертається, може використовуватися з іншими функціями сокету.

### Список параметрів

`address`

Екземпляр [AddressInfo](class.addressinfo.md), створений за допомогою [socketaddrinfolookup()](function.socket-addrinfo-lookup.md)

### Значення, що повертаються

Повертає екземпляр [Socket](class.socket.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |
|  | `address` тепер екземпляр класу [AddressInfo](class.addressinfo.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socketaddrinfobind()](function.socket-addrinfo-bind.md) - Створити та прив'язати до сокету із вказаного addrinfo
-   [socketaddrinfoexplain()](function.socket-addrinfo-explain.md) - Отримати інформацію про addrinfo
-   [socketaddrinfolookup()](function.socket-addrinfo-lookup.md) - Отримати масив з вмістом getaddrinfo про вказане ім'я хоста
