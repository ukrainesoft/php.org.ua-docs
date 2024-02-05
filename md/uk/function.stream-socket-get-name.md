---
navigation:
  - function.stream-socket-enable-crypto.md: « stream\_socket\_enable\_crypto
  - function.stream-socket-pair.md: stream\_socket\_pair »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_get\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_get\_name

(PHP 5, PHP 7, PHP 8)

stream\_socket\_get\_name — Отримати назву локального або віддаленого сокету

### Опис

```methodsynopsis
stream_socket_get_name(resource $socket, bool $remote): string|false
```

Повертає локальну або віддалену назву вказаного сокетного з'єднання.

### Список параметрів

`socket`

Сокет, назву якого потрібно отримати.

`remote`

Если установлено в\*\*`true`**, то буде повернуто `віддалене`название сокета, если установлено в**`false`\*\*, то буде повернуто `локальне`название.

### Значення, що повертаються

Название сокета или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [stream\_socket\_accept()](function.stream-socket-accept.md) \- Приймати з'єднання в сокеті, створеному за допомогою функції stream\_socket\_server
