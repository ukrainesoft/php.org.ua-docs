---
navigation:
  - function.socket-setopt.html: « socketsetopt
  - function.socket-strerror.html: socketstrerror »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
title: socketshutdown
---
# socketshutdown

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketshutdown — Завершує роботу сокету на отримання та/або відправлення даних

### Опис

```methodsynopsis
socket_shutdown(Socket $socket, int $mode = 2): bool
```

Функція **socketshutdown()** дозволяє вам зупинити передачу вступників, вихідних або всіх даних (за замовчуванням) через сокет `socket`

> **Зауваження**
> 
> Асоційований буфер, або буфери, можуть бути звільнені, а можуть і ні.

### Список параметрів

`socket`

Екземпляр [Socket](class.socket.html), створений за допомогою функції [socketcreate()](function.socket-create.html)

`mode`

Значення параметру `mode` може бути одним з наступних:

<table class="doctable table"><caption><strong>можливі значення для параметра <code class="parameter">mode</code></strong></caption><tbody class="tbody"><tr><td><code class="literal">0</code></td><td>Завершує читання із сокету</td></tr><tr><td><code class="literal">1</code></td><td>Завершує запис у сокет</td></tr><tr><td><code class="literal">2</code></td><td>Завершує читання та запис у сокет</td></tr></tbody></table>

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `socket` тепер екземпляр класу [Socket](class.socket.html); раніше був ресурсом (resource). |
