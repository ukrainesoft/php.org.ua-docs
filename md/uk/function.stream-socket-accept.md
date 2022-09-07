---
navigation:
  - function.stream-set-write-buffer.md: « streamsetwritebuffer
  - function.stream-socket-client.md: streamsocketclient »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsocketaccept
---
# streamsocketaccept

(PHP 5, PHP 7, PHP 8)

streamsocketaccept — Приймати з'єднання в сокеті, створеному за допомогою функції [streamsocketserver()](function.stream-socket-server.md)

### Опис

```methodsynopsis
stream_socket_accept(resource $socket, ?float $timeout = null, string &$peer_name = null): resource|false
```

Приймати з'єднання в сокеті, попередньо створеному за допомогою функції [streamsocketserver()](function.stream-socket-server.md)

### Список параметрів

`socket`

Серверний сокет для прийняття з'єднання.

`timeout`

Перевизначити час очікування на підключення за замовчуванням. Час має бути вказано за секунди. За замовчуванням використовується значення [defaultsockettimeout](filesystem.configuration.md#ini.default-socket-timeout)

`peer_name`

Буде присвоєно ім'я (адресу) клієнта, який приєднався, якщо воно міститься та доступне з вибраного транспорту.

> **Зауваження**
> 
> Можливо визначено пізніше, використовуючи функцію [streamsocketgetname()](function.stream-socket-get-name.md)

### Значення, що повертаються

Повертає потік прийнятого з'єднання з сокетом або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `timeout` тепер допускає значення null. |

### Примітки

**Увага**

Ця функція не повинна використовуватись із серверними сокетами UDP. Натомість використовуйте [streamsocketrecvfrom()](function.stream-socket-recvfrom.md) і [streamsocketsendto()](function.stream-socket-sendto.md)

### Дивіться також

-   [streamsocketserver()](function.stream-socket-server.md) - Створює інтернет-сокет або доменний сокет Unix
-   [streamsocketgetname()](function.stream-socket-get-name.md) - Отримати назву локального чи віддаленого сокету
-   [streamsetblocking()](function.stream-set-blocking.md) - Встановити блокуючий/неблокуючий режим у потоці
-   [streamsettimeout()](function.stream-set-timeout.md) - Встановити значення часу очікування потоку
-   [fgets()](function.fgets.md) - Читає рядок із файлу
-   [fgetss()](function.fgetss.md) - Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.md) - Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.md) - Закриває відкритий дескриптор файлу
-   [feof()](function.feof.md) - Перевіряє, чи кінець файлу досягнуто
-   [Функции cURL](ref.curl.md)
