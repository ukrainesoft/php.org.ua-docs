---
navigation:
  - function.stream-socket-enable-crypto.md: « streamsocketenablecrypto
  - function.stream-socket-pair.md: streamsocketpair »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsocketgetname
---
# streamsocketgetname

(PHP 5, PHP 7, PHP 8)

streamsocketgetname — Отримати назву локального або віддаленого сокету

### Опис

```methodsynopsis
stream_socket_get_name(resource $socket, bool $remote): string|false
```

Повертає локальну або віддалену назву вказаного сокетного з'єднання.

### Список параметрів

`socket`

Сокет, назву якого потрібно отримати.

`remote`

Якщо встановлено **`true`**, то буде повернуто `удалённое` назву сокету, якщо встановлено **`false`**, то буде повернуто `локальное` назву.

### Значення, що повертаються

Назва сокету або **`false`** у разі виникнення помилки.

### Дивіться також

-   [streamsocketaccept()](function.stream-socket-accept.md) - Приймати з'єднання в сокеті, створеному за допомогою функції streamsocketserver
