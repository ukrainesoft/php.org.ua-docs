---
navigation:
  - function.socket-setopt.md: « socket\_setopt
  - function.socket-strerror.md: socket\_strerror »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_shutdown
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_shutdown

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_shutdown — Завершує роботу сокету на отримання та/або відправлення даних

### Опис

```methodsynopsis
socket_shutdown(Socket $socket, int $mode = 2): bool
```

Функция**socket\_shutdown()** дозволяє вам зупинити передачу вступників, вихідних або всіх даних (за замовчуванням) через сокет `socket`

> **Зауваження** :
> 
> Асоційований буфер, або буфери, можуть бути звільнені, а можуть і ні.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.md), створений за допомогою функції [socket\_create()](function.socket-create.md)

`mode`

Значение параметра`mode` може бути одним з наступних:

<table class="doctable table"><caption><strong>можливі значення для параметра <code class="parameter">mode</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">0</code></td><td>Завершує читання із сокету</td></tr><tr><td><code class="literal">1</code></td><td>Завершує запис у сокет</td></tr><tr><td><code class="literal">2</code></td><td>Завершує читання та запис у сокет</td></tr></tbody></table>

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `socket` тепер екземпляр класу [Socket](class.socket.md); раніше був ресурсом (resource). |
