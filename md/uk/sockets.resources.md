---
navigation:
  - sockets.configuration.md: « Налаштування під час виконання
  - sockets.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - sockets.setup.md: Встановлення та налаштування
title: Типи ресурсів
---
## Типи ресурсів

До PHP 8.0.0, [socketaccept()](function.socket-accept.md) [socketimportstream()](function.socket-import-stream.md) [socketaddrinfoconnect()](function.socket-addrinfo-connect.md) [socketaddrinfobind()](function.socket-addrinfo-bind.md) [socketcreatelisten()](function.socket-create-listen.md) [socketwsaprotocolinfoimport()](function.socket-wsaprotocol-info-import.md) і [socketcreate()](function.socket-create.md) повертали ресурси сокетів.

До PHP 8.0, [socketaddrinfolookup()](function.socket-addrinfo-lookup.md) повертала масив ресурсів AddressInfo.
