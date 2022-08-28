Функції для роботи з потоками

-   [« streamWrapper::url\_stat](streamwrapper.url-stat.html)
    
-   [stream\_bucket\_append »](function.stream-bucket-append.html)
    
-   [PHP Manual](index.html)
    
-   [Потоки](book.stream.html)
    
-   Функції для роботи з потоками
    

# Функції для роботи з потоками

## Зміст

-   [stream\_bucket\_append](function.stream-bucket-append.html) - Додати відро (bucket) до бригади (brigade)
-   [stream\_bucket\_make\_writeable](function.stream-bucket-make-writeable.html) — Повертає об'єкт кошика із бригади для подальшої роботи з ним
-   [stream\_bucket\_new](function.stream-bucket-new.html) — Створити нове цебро для використання в поточному потоці
-   [stream\_bucket\_prepend](function.stream-bucket-prepend.html) — Додати відро на початок бригади
-   [stream\_context\_create](function.stream-context-create.html) - Створює контекст потоку
-   [stream\_context\_get\_default](function.stream-context-get-default.html) — Отримує контекст потоку за умовчанням
-   [stream\_context\_get\_options](function.stream-context-get-options.html) — Отримує опції для потоку/обгортки/контексту
-   [stream\_context\_get\_params](function.stream-context-get-params.html) — Отримує параметри із контексту
-   [stream\_context\_set\_default](function.stream-context-set-default.html) — Встановити контекст потоку за промовчанням
-   [stream\_context\_set\_option](function.stream-context-set-option.html) — Встановлює опцію для потоку/обгортки/контексту
-   [stream\_context\_set\_params](function.stream-context-set-params.html) — Встановлює параметри потоку/обгортки/контексту
-   [stream\_copy\_to\_stream](function.stream-copy-to-stream.html) — Копіює дані з одного потоку до іншого
-   [stream\_filter\_append](function.stream-filter-append.html) — Прикріпити фільтр до потоку
-   [stream\_filter\_prepend](function.stream-filter-prepend.html) - Прикріплює фільтр до потоку
-   [stream\_filter\_register](function.stream-filter-register.html) — Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_remove](function.stream-filter-remove.html) — Видалити фільтр із потоку
-   [stream\_get\_contents](function.stream-get-contents.html) — Читає частину потоку, що залишилася, в рядок
-   [stream\_get\_filters](function.stream-get-filters.html) — Отримати список зареєстрованих фільтрів
-   [stream\_get\_line](function.stream-get-line.html) — Отримує рядок із потокового ресурсу до вказаного роздільника
-   [stream\_get\_meta\_data](function.stream-get-meta-data.html) — Витягує заголовок/метадані з потоків/файлових покажчиків
-   [stream\_get\_transports](function.stream-get-transports.html) - Отримати список зареєстрованих транспортів сокету
-   [stream\_get\_wrappers](function.stream-get-wrappers.html) — Отримати список зареєстрованих потоків
-   [stream\_is\_local](function.stream-is-local.html) — Перевіряє, чи потік є локальним потоком
-   [stream\_isatty](function.stream-isatty.html) — Перевіряє, чи є потік TTY
-   [stream\_notification\_callback](function.stream-notification-callback.html) — Callback-функція параметра контексту notification
-   [stream\_register\_wrapper](function.stream-register-wrapper.html) - Псевдонім streamwrapperregister
-   [stream\_resolve\_include\_path](function.stream-resolve-include-path.html) — Перетворити повне ім'я файлу, використовуючи шляхи увімкнення
-   [stream\_select](function.stream-select.html) — Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [stream\_set\_blocking](function.stream-set-blocking.html) — Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_chunk\_size](function.stream-set-chunk-size.html) — Встановити розмір фрагмента даних потоку
-   [stream\_set\_read\_buffer](function.stream-set-read-buffer.html) — Встановити буферизацію читання файлу на вказаному потоці
-   [stream\_set\_timeout](function.stream-set-timeout.html) — Встановити час очікування для потоку
-   [stream\_set\_write\_buffer](function.stream-set-write-buffer.html) — Встановлює буферизацію файлу під час запису у вказаний потік
-   [stream\_socket\_accept](function.stream-socket-accept.html) — Приймати з'єднання в сокеті, створеному за допомогою функції streamsocketserver
-   [stream\_socket\_client](function.stream-socket-client.html) — Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_socket\_enable\_crypto](function.stream-socket-enable-crypto.html) — Вмикає або вимикає шифрування на вже підключеному сокеті
-   [stream\_socket\_get\_name](function.stream-socket-get-name.html) — Отримати назву локального чи віддаленого сокету
-   [stream\_socket\_pair](function.stream-socket-pair.html) — Створює пару підключених, невиразних потоків сокетів
-   [stream\_socket\_recvfrom](function.stream-socket-recvfrom.html) — Отримує дані із сокету, підключеного чи ні
-   [stream\_socket\_sendto](function.stream-socket-sendto.html) — Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
-   [stream\_socket\_server](function.stream-socket-server.html) - Створює інтернет-сокет або доменний сокет Unix
-   [stream\_socket\_shutdown](function.stream-socket-shutdown.html) — Закрити повнодуплексне з'єднання
-   [stream\_supports\_lock](function.stream-supports-lock.html) — Визначає, чи потік підтримує блокування
-   [stream\_wrapper\_register](function.stream-wrapper-register.html) - Реєструє обгортку URL, реалізовану у вигляді PHP-класу
-   [stream\_wrapper\_restore](function.stream-wrapper-restore.html) — Відновлює скасовану раніше вбудовану обгортку
-   [stream\_wrapper\_unregister](function.stream-wrapper-unregister.html) — Скасує реєстрацію обгортки URL