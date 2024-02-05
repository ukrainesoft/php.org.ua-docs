---
navigation:
  - function.socket-addrinfo-explain.md: « socket\_addrinfo\_explain
  - function.socket-atmark.md: socket\_atmark »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_addrinfo\_lookup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_addrinfo\_lookup

(PHP 7 >= 7.2.0, PHP 8)

socket\_addrinfo\_lookup — Отримати масив із вмістом getaddrinfo про вказане ім'я хоста

### Опис

```methodsynopsis
socket_addrinfo_lookup(string $host, ?string $service = null, array $hints = []): array|false
```

Пошук різних способів підключення до хоста (`host`). Масив, що повертається, містить набір екземплярів. [AddressInfo](class.addressinfo.md), які можна прив'язати за допомогою [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.md)

### Список параметрів

`host`

Ім'я хоста для пошуку.

`service`

Сервіс для підключення Якщо значення є числовим рядком, воно означає порт. В іншому випадку це ім'я мережної служби, яке зіставляється з портом операційної системи.

`hints`

Підказки надають критерії вибору адрес, що повертаються. Ви можете вказати підказки, як визначено getaddrinfo.

### Значення, що повертаються

Повертає масив екземплярів [AddressInfo](class.addressinfo.md), які можна використовувати з іншими функціями socket\_addrinfo. У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає масив екземплярів [AddressInfo](class.addressinfo.md); раніше повертався ресурс (resource). |
| 8.0.0 | `service` тепер допускає значення null. |

### Дивіться також

-   [socket\_addrinfo\_bind()](function.socket-addrinfo-bind.md) \- Створити та прив'язати до сокету із зазначеного addrinfo
-   [socket\_addrinfo\_connect()](function.socket-addrinfo-connect.md) \- Створити та підключитися до сокету із зазначеного addrinfo
-   [socket\_addrinfo\_explain()](function.socket-addrinfo-explain.md) \- Отримати інформацію про addrinfo
