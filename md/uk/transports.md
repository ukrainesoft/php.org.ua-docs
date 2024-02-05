---
navigation:
  - filters.encryption.md: « Шифруючі фільтри
  - transports.inet.md: 'Інтернет-сокети: TCP, UDP, SSL та TLS »'
  - index.md: PHP Manual
  - appendices.md: Програми
title: Список підтримуваних транспортних протоколів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Список підтримуваних транспортних протоколів

## Зміст

-   [Інтернет-сокети: TCP, UDP, SSL та TLS](transports.inet.md)
-   [Unix-сокети: UNIX та UDG](transports.unix.md)

Нижченаведений список містить інформацію про протоколи передачі, вбудовані в PHP і готові для використання функціями роботи з сокетами, такими як [fsockopen()](function.fsockopen.md) і [stream\_socket\_client()](function.stream-socket-client.md). Ці протоколи *не*применяются в[модулях для роботи із Сокетами](ref.sockets.md)

Для отримання списку підтримуваних протоколів передачі, вбудованих у вашу версію PHP, використовуйте функцію [stream\_get\_transports()](function.stream-get-transports.md)
