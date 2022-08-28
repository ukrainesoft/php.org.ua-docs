Приймати з'єднання в сокеті, створеному за допомогою функції streamsocketserver

-   [« stream\_set\_write\_buffer](function.stream-set-write-buffer.html)
    
-   [stream\_socket\_client »](function.stream-socket-client.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Приймати з'єднання в сокеті, створеному за допомогою функції streamsocketserver
    

# streamsocketaccept

(PHP 5, PHP 7, PHP 8)

streamsocketaccept — Приймати з'єднання в сокеті, створеному за допомогою функції [stream\_socket\_server()](function.stream-socket-server.html)

### Опис

```methodsynopsis
stream_socket_accept(resource $socket, ?float $timeout = null, string &$peer_name = null): resource|false
```

Приймати з'єднання в сокеті, попередньо створеному за допомогою функції [stream\_socket\_server()](function.stream-socket-server.html)

### Список параметрів

`socket`

Серверний сокет для прийняття з'єднання.

`timeout`

Перевизначити час очікування на підключення за замовчуванням. Час має бути вказано за секунди. За замовчуванням використовується значення [default\_socket\_timeout](filesystem.configuration.html#ini.default-socket-timeout)

`peer_name`

Буде присвоєно ім'я (адресу) клієнта, який приєднався, якщо воно міститься та доступне з вибраного транспорту.

> **Зауваження**
> 
> Можливо визначено пізніше, використовуючи функцію [stream\_socket\_get\_name()](function.stream-socket-get-name.html)

### Значення, що повертаються

Повертає потік прийнятого з'єднання з сокетом або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `timeout` тепер допускає значення null. |

### Примітки

**Увага**

Ця функція не повинна використовуватись із серверними сокетами UDP. Натомість використовуйте [stream\_socket\_recvfrom()](function.stream-socket-recvfrom.html) і [stream\_socket\_sendto()](function.stream-socket-sendto.html)

### Дивіться також

-   [stream\_socket\_server()](function.stream-socket-server.html) - Створює інтернет-сокет або доменний сокет Unix
-   [stream\_socket\_get\_name()](function.stream-socket-get-name.html) - Отримати назву локального чи віддаленого сокету
-   [stream\_set\_blocking()](function.stream-set-blocking.html) - Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_timeout()](function.stream-set-timeout.html) - Встановити значення часу очікування потоку
-   [fgets()](function.fgets.html) - Читає рядок із файлу
-   [fgetss()](function.fgetss.html) - Читає рядок з файлу та видаляє HTML-теги
-   [fwrite()](function.fwrite.html) - Бінарно-безпечний запис у файл
-   [fclose()](function.fclose.html) - Закриває відкритий дескриптор файлу
-   [feof()](function.feof.html) - Перевіряє, чи кінець файлу досягнуто
-   [Функции cURL](ref.curl.html)