---
navigation:
  - function.stream-socket-recvfrom.md: « stream\_socket\_recvfrom
  - function.stream-socket-server.md: stream\_socket\_server »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_sendto
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_sendto

(PHP 5, PHP 7, PHP 8)

stream\_socket\_sendto — Надсилає повідомлення до сокету, незалежно від того, приєднаний він чи ні

### Опис

```methodsynopsis
stream_socket_sendto(    resource $socket,    string $data,    int $flags = 0,    string $address = ""): int|false
```

Надсилає зазначені дані `data`через сокет`socket`

### Список параметрів

`socket`

Сокет для надсилання даних `data`

`data`

Надані дані.

`flags`

Значение параметра`flags` може бути будь-якою з наступних комбінацій:

<table class="doctable table"><caption><strong>можливі значення для параметра <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><strong><code>STREAM_OOB</code></strong></td><td>Обробляти OOB (out-of-band, позасмугові) дані.</td></tr></tbody></table>

`address`

Адреса, вказана при створенні потокового сокету, буде використовуватися доти, доки не вказана альтернативна адреса в параметрі `address`

Якщо вказано, він має бути у форматі ipv4 або ipv6.

### Значення, що повертаються

Повертає код результату як ціле число або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**stream\_socket\_sendto()\*\*\*\*

```php
<?php
/* Открыть сокет на 1234-м порту на localhost */
$socket = stream_socket_client('tcp://127.0.0.1:1234');

/* Отправить обычные данные через обычные каналы. */
fwrite($socket, "Передача обычных данных.");

/* Отправляем внеполосные данные. */
stream_socket_sendto($socket, "Внеполосные данные.", STREAM_OOB);

/* Закрыть сокет */
fclose($socket);
?>
```

### Дивіться також

-   [stream\_socket\_recvfrom()](function.stream-socket-recvfrom.md) \- Отримує дані із сокету, підключеного чи ні
-   [stream\_socket\_client()](function.stream-socket-client.md) \- Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_socket\_server()](function.stream-socket-server.md) \- Створює інтернет-сокет або доменний сокет Unix
