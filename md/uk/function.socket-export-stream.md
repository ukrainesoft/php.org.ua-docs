---
navigation:
  - function.socket-create.md: « socket\_create
  - function.socket-get-option.md: socket\_get\_option »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_export\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_export\_stream

(PHP 7 >= 7.0.7, PHP 8)

socket\_export\_stream — Експортувати сокет у потік, що інкапсулює сокет

### Опис

```methodsynopsis
socket_export_stream(Socket $socket): resource|false
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`socket`

### Значення, що повертаються

Повертає ресурс або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
