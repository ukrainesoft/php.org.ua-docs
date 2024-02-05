---
navigation:
  - function.stream-socket-pair.md: « stream\_socket\_pair
  - function.stream-socket-sendto.md: stream\_socket\_sendto »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_recvfrom
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_recvfrom

(PHP 5, PHP 7, PHP 8)

stream\_socket\_recvfrom — Отримує дані із сокету, підключеного чи ні

### Опис

```methodsynopsis
stream_socket_recvfrom(    resource $socket,    int $length,    int $flags = 0,    ?string &$address = null): string|false
```

**stream\_socket\_recvfrom()** приймає дані з віддаленого сокету розміром до `length`байт.

### Список параметрів

`socket`

Віддалений сокет.

`length`

Количество байт для получения из параметра`socket`

`flags`

Значение параметра`flags` може бути будь-якою комбінацією з наступного:

<table class="doctable table"><caption><strong>Можливі значення для параметра <code class="parameter">flags</code></strong></caption><tbody class="tbody"><tr><td><strong><code>STREAM_OOB</code></strong></td><td>Обробляти дані OOB (<code class="literal">out-of-band</code>).&lt; /td&gt;</td></tr><tr><td><strong><code>STREAM_PEEK</code></strong></td><td>Отримувати дані з сокету, але не витрачати буфер. Наступні виклики функцій <span class="function"><a href="function.fread.md" class="function">fread()</a></span> або <span class="function"><strong>stream_socket_recvfrom()</strong></span> отримають ті самі дані.</td></tr></tbody></table>

`address`

Если указан параметр`address`, він буде заповнений адресою віддаленого сокету.

### Значення, що повертаються

Повертає прочитані дані у вигляді рядка або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад использования функции**stream\_socket\_recvfrom()\*\*\*\*

```php
<?php
/* Открывает серверный сокет на 1234-м порту на localhost */
$server = stream_socket_server('tcp://127.0.0.1:1234');

/* Принимает соединение */
$socket = stream_socket_accept($server);

/* Получает пакет (обычный размер MTU 1500) OOB-данных */
echo "Получены данные OOB (Out-Of-Band): '" . stream_socket_recvfrom($socket, 1500, STREAM_OOB) . "'\n";

/* Получить обычные данные, но не расходовать их. */
echo "Данные: '" . stream_socket_recvfrom($socket, 1500, STREAM_PEEK) . "'\n";

/* Получить тот же самый пакет снова, но в этот раз удалить его из буфера данных. */
echo "Данные: '" . stream_socket_recvfrom($socket, 1500) . "'\n";

/* Закрыть сокет */
fclose($socket);
fclose($server);
?>
```

### Примітки

> **Зауваження** :
> 
> Якщо отримане повідомлення довжиною більше, ніж параметр `length`, зайві байти можуть бути пропущені в залежності від типу сокету, з якого отримано повідомлення (наприклад, UDP).

> **Зауваження** :
> 
> Виклики функції **stream\_socket\_recvfrom()** на потоках, заснованих на сокетах, після викликів потокових функцій, що базуються на буферах (таких як [fread()](function.fread.md) або [stream\_get\_line()](function.stream-get-line.md)) читають дані безпосередньо із сокету та пропускають потоковий буфер.

### Дивіться також

-   [stream\_socket\_sendto()](function.stream-socket-sendto.md) \- Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
-   [stream\_socket\_client()](function.stream-socket-client.md) \- Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_socket\_server()](function.stream-socket-server.md) \- Створює інтернет-сокет або доменний сокет Unix
