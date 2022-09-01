---
navigation:
  - filters.encryption.md: « Шифруючі фільтри
  - transports.inet.md: 'Інтернет-сокети: TCP, UDP, SSL та TLS »'
  - index.md: PHP Manual
  - appendices.md: Appendices
title: Список підтримуваних транспортних протоколів
---
# Список підтримуваних транспортних протоколів

## Зміст

-   [Інтернет-сокети: TCP, UDP, SSL та TLS](transports.inet.md)
-   [Unix-сокети: UNIX та UDG](transports.unix.md)

Нижченаведений список містить інформацію про протоколи передачі, вбудовані в PHP і готові для використання функціями роботи з сокетами, такими як [fsockopen()](function.fsockopen.md) і [streamsocketclient()](function.stream-socket-client.html). Ці протоколи *не* застосовуються в [модулях для роботи із Сокетами](ref.sockets.md)

Для отримання списку підтримуваних протоколів передачі, вбудованих у вашу версію PHP, використовуйте функцію [streamgettransports()](function.stream-get-transports.html)
