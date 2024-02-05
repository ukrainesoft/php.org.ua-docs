---
navigation:
  - function.socket-accept.md: « socket\_accept
  - function.socket-addrinfo-connect.md: socket\_addrinfo\_connect »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_addrinfo\_bind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_addrinfo\_bind

(PHP 7 >= 7.2.0, PHP 8)

socket\_addrinfo\_bind — Створити та прив'язати до сокету із вказаного addrinfo

### Опис

```methodsynopsis
socket_addrinfo_bind(AddressInfo $address): Socket|false
```

Створити екземпляр [Socket](class.socket.md) та прив'язати його з наданим [AddressInfo](class.addressinfo.md). Значення цієї функції, що повертається, може використовуватися з [socket\_listen()](function.socket-listen.md)

### Список параметрів

`address`

Екземпляр [AddressInfo](class.addressinfo.md), створений за допомогою [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.md)

### Значення, що повертаються

Повертає екземпляр [Socket](class.socket.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [Socket](class.socket.md); раніше повертався ресурс (resource). |
| 8.0.0 | `address` тепер екземпляр класу [AddressInfo](class.addressinfo.md); раніше був ресурсом (resource). |

### Дивіться також

-   [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.md) \- Створити та підключитися до сокету із зазначеного addrinfo
-   [socket\_addrinfo\_explain()](function.socket-addrinfo-explain.md) \- Отримати інформацію про addrinfo
-   [socket\_addrinfo\_lookup()](function.socket-addrinfo-lookup.md) \- Отримати масив з вмістом getaddrinfo про вказане ім'я хоста
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
