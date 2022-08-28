Обумовлені константи

-   [« Классы для работы с потоками](stream.resources.html)
    
-   [Потоковые фильтры »](stream.filters.html)
    
-   [PHP Manual](index.html)
    
-   [Потоки](book.stream.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

| Константа | Описание |
| --- | --- |
| **`STREAM_FILTER_READ`** | Використовується у функціях [stream\_filter\_append()](function.stream-filter-append.html) і [stream\_filter\_prepend()](function.stream-filter-prepend.html). Вказує на те, що заданий фільтр може використовуватись лише в операціях читання (*reading* |
| **`STREAM_FILTER_WRITE`** | Використовується у функціях [stream\_filter\_append()](function.stream-filter-append.html) і [stream\_filter\_prepend()](function.stream-filter-prepend.html). Вказує на те, що заданий фільтр може використовуватись тільки в операціях запису (*writing* |
| **`STREAM_FILTER_ALL`** | Еквівалентно запису \`STREAM\_FILTER\_READ |
| **`PSFS_PASS_ON`** | `Return Code` вказує, що фільтр користувача повернув бакети (buckets) в `$out` |
| **`PSFS_FEED_ME`** | `Return Code` вказує, що фільтр користувача не повернув бакети (buckets) в `$out`. (тобто немає доступних даних). |
| **`PSFS_ERR_FATAL`** | `Return Code` вказує, що фільтр користувача викликав необроблювану помилку (тобто. отримані невірні дані). |
| **`PSFS_FLAG_NORMAL`** | Нормальне читання/запис. |
| **`PSFS_FLAG_FLUSH_INC`** | Додаткове архівування. |
| **`PSFS_FLAG_FLUSH_CLOSE`** | Збереження на диск перед закриттям. |
| **`STREAM_USE_PATH`** | Прапор (`Flag`), який вказує, що `stream` використовує шлях, що підключається (include path). |
| **`STREAM_REPORT_ERRORS`** | Прапор (`Flag`) що вказує, що `wrapper` може викидати винятки в процесі відкриття потоку функцією [trigger\_error()](function.trigger-error.html) Якщо цей прапор не встановлено, викликати помилки не варто. |
| **`STREAM_CLIENT_ASYNC_CONNECT`** | Асинхронне відкриття з'єднання із клієнтським сокетом. Ця установка повинна використовуватися спільно з прапором **`STREAM_CLIENT_CONNECT`**. Використовується у функції [stream\_socket\_client()](function.stream-socket-client.html) |
| **`STREAM_CLIENT_CONNECT`** | Відкриття з'єднання із клієнтським сокетом. Клієнтські сокети завжди повинні містити цей прапор. Використовується функцією [stream\_socket\_client()](function.stream-socket-client.html) |
| **`STREAM_CLIENT_PERSISTENT`** | Клієнтський сокет, відкритий функцією [stream\_socket\_client()](function.stream-socket-client.html) залишатиметься відкритим між завантаженнями сторінок. |
| **`STREAM_SERVER_BIND`** | Повідомляє потоку, створеному функцією [stream\_socket\_server()](function.stream-socket-server.html)зв'язатися із заданою метою. Серверні сокети завжди повинні містити цей прапор. |
| **`STREAM_SERVER_LISTEN`** | Вказує потоку, створеному функцією [stream\_socket\_server()](function.stream-socket-server.html) та пов'язаного прапором **`STREAM_SERVER_BIND`**почати слухати сокет. Передачі даних, що встановлюють з'єднання (як TCP), повинні використовувати цей прапор, інакше сокет не увімкнеться. Використання цього прапора під час передачі без встановлення з'єднання (як UDP) викликає помилку. |
| **`STREAM_NOTIFY_RESOLVE`** | Необхідна для потоку адреса віддаленого ресурсу визначена, або це визначення завершилося невдачею. Щоб дізнатися, що саме сталося, дивіться `severity` |
| **`STREAM_NOTIFY_CONNECT`** | З'єднання із зовнішнім ресурсом встановлено. |
| **`STREAM_NOTIFY_AUTH_REQUIRED`** | Для доступу до заданого ресурсу потрібна додаткова авторизація. Зазвичай видається у помилці рівня `severity` **`STREAM_NOTIFY_SEVERITY_ERR`** |
| **`STREAM_NOTIFY_MIME_TYPE_IS`** | `mime-type` ресурсу ідентифіковано. Опис знайденого типу можна переглянути у параметрі `message` |
| **`STREAM_NOTIFY_FILE_SIZE_IS`** | Розмір (`size`) ресурсу визначено. |
| **`STREAM_NOTIFY_REDIRECTED`** | Зовнішній ресурс перенаправив потік на інше місце. Додатково дивись `message` |
| **`STREAM_NOTIFY_PROGRESS`** | Індикатор поточного процесу передачі через потік. Можна дізнатися, скільки передано (`bytes_transferred`), і скільки всього байт (`bytes_max` |
| **`STREAM_NOTIFY_COMPLETED`** | У потоці немає доступних даних. |
| **`STREAM_NOTIFY_FAILURE`** | Загальна помилка під час роботи з потоком. Деталі дивіться у `message` і `message_code` |
| **`STREAM_NOTIFY_AUTH_RESULT`** | Авторизація завершена (незалежно від успіху авторизації). |
| **`STREAM_NOTIFY_SEVERITY_INFO`** | Звичайне повідомлення, яке не стосується помилок. |
| **`STREAM_NOTIFY_SEVERITY_WARN`** | Некритична помилка. Можна продовжити роботу. |
| **`STREAM_NOTIFY_SEVERITY_ERR`** | Критична помилка. Продовження роботи неможливе. |
| **`STREAM_IPPROTO_ICMP`** | Надає ICMP-сокет. |
| **`STREAM_IPPROTO_IP`** | Надає IP-сокет. |
| **`STREAM_IPPROTO_RAW`** | Надає RAW сокет. |
| **`STREAM_IPPROTO_TCP`** | Надає TCP-сокет. |
| **`STREAM_IPPROTO_UDP`** | Надає UDP-сокет. |
| **`STREAM_PF_INET`** | Інтернет протокол 4 версії (IPv4). |
| **`STREAM_PF_INET6`** | Інтернет-протокол 6 версії (IPv6). |
| **`STREAM_PF_UNIX`** | Внутрішні протоколи Unix. |
| **`STREAM_SOCK_DGRAM`** | Надає датаграми – повідомлення без встановлення з'єднання (UDP, наприклад). |
| **`STREAM_SOCK_RAW`** | Надає необроблений (raw) сокет, який дає доступ до внутрішніх мережевих протоколів та інтерфейсів. Зазвичай сокети цього доступні лише root-пользователям. |
| **`STREAM_SOCK_RDM`** | Надає сокет RDM (Reliably-delivered messages). |
| **`STREAM_SOCK_SEQPACKET`** | Надає сокет послідовного потоку пакетів. |
| **`STREAM_SOCK_STREAM`** | Надає послідовні двонаправлені байтові потоки з механізмом передачі даних (TCP, наприклад). |
| **`STREAM_SHUT_RD`** | Використовується функцією [stream\_socket\_shutdown()](function.stream-socket-shutdown.html) для відключення подальшого прийому даних. |
| **`STREAM_SHUT_WR`** | Використовується функцією [stream\_socket\_shutdown()](function.stream-socket-shutdown.html) для відключення подальшої передачі. |
| **`STREAM_SHUT_RDWR`** | Використовується функцією [stream\_socket\_shutdown()](function.stream-socket-shutdown.html) для відключення подальших прийому та передачі даних. |
| **`STREAM_CAST_FOR_SELECT`** | Розподіл потоків, використовується, коли функція [stream\_select()](function.stream-select.html) викликає **streamcast()** |
| **`STREAM_CAST_AS_STREAM`** | Розподіл потоків, використовується, коли функція **streamcast()** викликається з іншого місця (дивіться вище). |
| **`STREAM_META_TOUCH`** | Використовується у функції **streammetadata()** для завдання виклику [touch()](function.touch.html) |
| **`STREAM_META_OWNER`** | Використовується у функції **streammetadata()** для завдання виклику [chown()](function.chown.html) |
| **`STREAM_META_OWNER_NAME`** | Використовується у функції **streammetadata()** для завдання виклику [chown()](function.chown.html) |
| **`STREAM_META_GROUP`** | Використовується у функції **streammetadata()** для завдання виклику [chgrp()](function.chgrp.html) |
| **`STREAM_META_GROUP_NAME`** | Використовується у функції **streammetadata()** для завдання виклику [chgrp()](function.chgrp.html) |
| **`STREAM_META_ACCESS`** | Використовується у функції **streammetadata()** для завдання виклику [chmod()](function.chmod.html) |
| **`STREAM_BUFFER_NONE`** | Без буферизації. |
| **`STREAM_BUFFER_LINE`** | Буферизація рядка. |
| **`STREAM_BUFFER_FULL`** | Повна буферизація. |

> **Зауваження**: Константи `+`, призначені для використання у функції [stream\_socket\_pair()](function.stream-socket-pair.html). Враховуйте, що деякі константи можуть бути недоступні у вашій системі.

> **Зауваження**: Константи **`STREAM_META_*`** призначені для використання у функції **streammetadata()**