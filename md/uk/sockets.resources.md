---
navigation:
  - sockets.configuration.md: « Налаштування під час виконання
  - sockets.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - sockets.setup.md: Встановлення та налаштування
title: Типи ресурсів
---
## Типи ресурсів

До PHP 8.0.0, [socketaccept()](function.socket-accept.html) [socketimportstream()](function.socket-import-stream.html) [socketaddrinfoconnect()](function.socket-addrinfo-connect.html) [socketaddrinfobind()](function.socket-addrinfo-bind.html) [socketcreatelisten()](function.socket-create-listen.html) [socketwsaprotocolinfoimport()](function.socket-wsaprotocol-info-import.html) і [socketcreate()](function.socket-create.html) повертали ресурси сокетів.

До PHP 8.0, [socketaddrinfolookup()](function.socket-addrinfo-lookup.html) повертала масив ресурсів AddressInfo.
