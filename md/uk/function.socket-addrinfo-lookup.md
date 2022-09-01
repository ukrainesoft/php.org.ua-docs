---
navigation:
  - function.socket-addrinfo-explain.html: « socketaddrinfoexplain
  - function.socket-bind.html: socketbind »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
title: socketaddrinfolookup
---
# socketaddrinfolookup

(PHP 7> = 7.2.0, PHP 8)

socketaddrinfolookup — Отримати масив із вмістом getaddrinfo про вказане ім'я хоста

### Опис

```methodsynopsis
socket_addrinfo_lookup(string $host, ?string $service = null, array $hints = []): array|false
```

Пошук різних способів підключення до хоста (`host`). Масив, що повертається, містить набір екземплярів. [AddressInfo](class.addressinfo.html), які можна прив'язати за допомогою [socketaddrinfobind()](function.socket-addrinfo-bind.html)

### Список параметрів

`host`

Ім'я хоста для пошуку.

`service`

Сервіс для підключення Якщо сервіс є ім'ям, він перетворюється на відповідний номер порту.

`hints`

Підказки надають критерії вибору адрес, що повертаються. Ви можете вказати підказки, як визначено getadrinfo.

### Значення, що повертаються

Повертає масив екземплярів [AddressInfo](class.addressinfo.html), які можна використовувати з іншими функціями socketaddrinfo. У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає масив екземплярів [AddressInfo](class.addressinfo.html); раніше повертався ресурс (resource). |
|  | `service` тепер допускає значення null. |

### Дивіться також

-   [socketaddrinfobind()](function.socket-addrinfo-bind.html) - Створити та прив'язати до сокету із зазначеного addrinfo
-   [socketaddrinfoconnect()](function.socket-addrinfo-connect.html) - Створити та підключитися до сокету із вказаного addrinfo
-   [socketaddrinfoexplain()](function.socket-addrinfo-explain.html) - Отримати інформацію про addrinfo
