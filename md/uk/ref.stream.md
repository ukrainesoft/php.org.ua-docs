---
navigation:
  - streamwrapper.url-stat.md: '« streamWrapper::url\_stat'
  - function.stream-bucket-append.md: stream\_bucket\_append »
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Функції для роботи з потоками
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції для роботи з потоками

## Зміст

-   [stream\_bucket\_append](function.stream-bucket-append.md) \- Додати бакет до бригади
-   [stream\_bucket\_make\_writeable](function.stream-bucket-make-writeable.md)— Повертає об'єкт бакета із бригади для подальшої роботи з ним
-   [stream\_bucket\_new](function.stream-bucket-new.md)— Створює новий бакет для використання у поточному потоці.
-   [stream\_bucket\_prepend](function.stream-bucket-prepend.md) \- Додає бакет на початок бригади
-   [stream\_context\_create](function.stream-context-create.md) \- Створює контекст потоку
-   [stream\_context\_get\_default](function.stream-context-get-default.md)— Отримує контекст потоку за умовчанням
-   [stream\_context\_get\_options](function.stream-context-get-options.md)— Отримує опції для потоку/обгортки/контексту
-   [stream\_context\_get\_params](function.stream-context-get-params.md)— Отримує параметри із контексту
-   [stream\_context\_set\_default](function.stream-context-set-default.md)— Встановити контекст потоку за промовчанням
-   [stream\_context\_set\_option](function.stream-context-set-option.md)— Встановлює опцію для потоку/обгортки/контексту
-   [stream\_context\_set\_options](function.stream-context-set-options.md)— Встановлює опції заданого контексту
-   [stream\_context\_set\_params](function.stream-context-set-params.md)— Встановлює параметри потоку/обгортки/контексту
-   [stream\_copy\_to\_stream](function.stream-copy-to-stream.md)— Копіює дані з одного потоку до іншого
-   [stream\_filter\_append](function.stream-filter-append.md)— Прикріпити фільтр до потоку
-   [stream\_filter\_prepend](function.stream-filter-prepend.md) \- Прикріплює фільтр до потоку
-   [stream\_filter\_register](function.stream-filter-register.md)— Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_remove](function.stream-filter-remove.md)— Видалити фільтр із потоку
-   [stream\_get\_contents](function.stream-get-contents.md)— Читає частину потоку, що залишилася, в рядок
-   [stream\_get\_filters](function.stream-get-filters.md)— Отримати список зареєстрованих фільтрів
-   [stream\_get\_line](function.stream-get-line.md)— Отримує рядок із потокового ресурсу до вказаного роздільника
-   [stream\_get\_meta\_data](function.stream-get-meta-data.md)— Витягує заголовок/метадані з потоків/файлових покажчиків
-   [stream\_get\_transports](function.stream-get-transports.md) \- Отримати список зареєстрованих транспортів сокету
-   [stream\_get\_wrappers](function.stream-get-wrappers.md)— Отримати список зареєстрованих потоків
-   [stream\_is\_local](function.stream-is-local.md)— Перевіряє, чи потік є локальним потоком
-   [stream\_isatty](function.stream-isatty.md)— Перевіряє, чи є потік TTY
-   [stream\_notification\_callback](function.stream-notification-callback.md)— Callback-функція параметра контексту notification
-   [stream\_register\_wrapper](function.stream-register-wrapper.md) \- Псевдонім stream\_wrapper\_register
-   [stream\_resolve\_include\_path](function.stream-resolve-include-path.md)— Перетворити повне ім'я файлу, використовуючи шляхи увімкнення
-   [stream\_select](function.stream-select.md)— Запускає еквівалент системного виклику select() на заданих масивах потоків з часом очікування, вказаним параметрами seconds та microseconds
-   [stream\_set\_blocking](function.stream-set-blocking.md)— Встановити блокуючий/неблокуючий режим у потоці
-   [stream\_set\_chunk\_size](function.stream-set-chunk-size.md)— Встановлює розмір фрагмента даних потоку
-   [stream\_set\_read\_buffer](function.stream-set-read-buffer.md)— Встановити буферизацію читання файлу на вказаному потоці
-   [stream\_set\_timeout](function.stream-set-timeout.md)— Встановити час очікування для потоку
-   [stream\_set\_write\_buffer](function.stream-set-write-buffer.md)— Встановлює буферизацію файлу під час запису у вказаний потік
-   [stream\_socket\_accept](function.stream-socket-accept.md)— Приймати з'єднання в сокеті, створеному за допомогою функції stream\_socket\_server
-   [stream\_socket\_client](function.stream-socket-client.md)— Відкрити з'єднання з інтернет-сокетом або доменним сокетом Unix
-   [stream\_socket\_enable\_crypto](function.stream-socket-enable-crypto.md)— Вмикає або вимикає шифрування на вже підключеному сокеті
-   [stream\_socket\_get\_name](function.stream-socket-get-name.md)— Отримати назву локального чи віддаленого сокету
-   [stream\_socket\_pair](function.stream-socket-pair.md)— Створює пару підключених, невиразних потоків сокетів
-   [stream\_socket\_recvfrom](function.stream-socket-recvfrom.md)— Отримує дані із сокету, підключеного чи ні
-   [stream\_socket\_sendto](function.stream-socket-sendto.md)— Надсилає повідомлення до сокету, незалежно від того, під'єднаний він чи ні
-   [stream\_socket\_server](function.stream-socket-server.md) \- Створює інтернет-сокет або доменний сокет Unix
-   [stream\_socket\_shutdown](function.stream-socket-shutdown.md)— Закрити повнодуплексне з'єднання
-   [stream\_supports\_lock](function.stream-supports-lock.md)— Визначає, чи потік підтримує блокування
-   [stream\_wrapper\_register](function.stream-wrapper-register.md) \- Реєструє обгортку URL, реалізовану у вигляді PHP-класу
-   [stream\_wrapper\_restore](function.stream-wrapper-restore.md)— Відновлює скасовану раніше вбудовану обгортку
-   [stream\_wrapper\_unregister](function.stream-wrapper-unregister.md)— Скасує реєстрацію обгортки URL
