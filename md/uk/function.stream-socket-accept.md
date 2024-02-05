---
navigation:
  - function.stream-set-write-buffer.md: « stream\_set\_write\_buffer
  - function.stream-socket-client.md: stream\_socket\_client »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_accept
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_accept

(PHP 5, PHP 7, PHP 8)

stream\_socket\_accept — Приймати з'єднання в сокеті, створеному за допомогою функції [stream\_socket\_server()](function.stream-socket-server.md)

### Опис

```methodsynopsis
stream_socket_accept(resource $socket, ?float $timeout = null, string &$peer_name = null): resource|false
```

Приймати з'єднання в сокеті, попередньо створеному за допомогою функції [stream\_socket\_server()](function.stream-socket-server.md)

### Список параметрів

`socket`

Серверний сокет для прийняття з'єднання.

`timeout`

Перевизначити час очікування на підключення за замовчуванням. Час має бути вказано за секунди. За замовчуванням використовується значення [default\_socket\_timeout](filesystem.configuration.md#ini.default-socket-timeout)

`peer_name`

Буде присвоєно ім'я (адресу) клієнта, який приєднався, якщо воно міститься та доступне з вибраного транспорту.

> **Зауваження** :
> 
> Можливо визначено пізніше, використовуючи функцію [stream\_socket\_get\_name()](function.stream-socket-get-name.md)

### Значення, що повертаються

Повертає потік прийнятого з'єднання з сокетом або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `timeout` тепер допускає значення null. |

### Примітки

**Увага**

Ця функція не повинна використовуватись із серверними сокетами UDP. Натомість використовуйте [stream\_socket\_recvfrom()](function.stream-socket-recvfrom.md) і [stream\_socket\_sendto()](function.stream-socket-sendto.md)

### Дивіться також

-   [stream\_socket\_server()](function.stream-socket-server.md) \- Створює інтернет-сокет або доменний сокет Unix
-   [stream\_socket\_get\_name()](function.stream-socket-get-name.md) \- Отримати назву локального чи віддаленого сокету
-   [stream\_set\_blocking()](function.stream-set-blocking.md) \- Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_timeout()](function.stream-set-timeout.md) \- Встановити значення часу очікування потоку
-   [fgets()](function.fgets.md) \- Читає рядок із файлу
-   [fgetss()](function.fgetss.md) \- Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.md) \- Закриває відкритий дескриптор файлу
-   [feof()](function.feof.md) \- Перевіряє, чи кінець файлу досягнуто
-   [Опції cURL](ref.curl.md)
