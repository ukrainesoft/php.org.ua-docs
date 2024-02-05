---
navigation:
  - memcached.installation.md: « Встановлення
  - memcached.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - memcached.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Memcached**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [memcached.sess\_locking](memcached.configuration.md#ini.memcached.sess-locking) | On | **`INI_ALL`** | Доступно з memcached 0.1.0. |
| [memcached.sess\_consistent\_hash](memcached.configuration.md#ini.memcached.sess-consistent-hash) | On | **`INI_ALL`** | Доступно з memcached 2.1.0. Значення за замовчуванням - `On`починаючи з memcached 3.0.0. |
| [memcached.sess\_binary](memcached.configuration.md#ini.memcached.sess-binary) | Off | **`INI_ALL`** | Доступно з memcached 2.0.0. Замінено на `memcached.sess_binary_protocol` в memcached 3.0.0. |
| [memcached.sess\_lock\_wait](memcached.configuration.md#ini.memcached.sess-lock-wait) | 150000 | **`INI_ALL`** | Доступно з memcached 0.1.0. Видалено в memcached 3.0.0. |
| [memcached.sess\_prefix](memcached.configuration.md#ini.memcached.sess-prefix) | memc.sess.key. | **`INI_ALL`** | Доступно з memcached 0.1.0. |
| [memcached.sess\_number\_of\_replicas](memcached.configuration.md#ini.memcached.sess-number-of-replicas) |  | **`INI_ALL`** | Доступно з memcached 2.1.0. |
| [memcached.sess\_randomize\_replica\_read](memcached.configuration.md#ini.memcached.sess-randomize-replica-read) | Off | **`INI_ALL`** | Доступно з memcached 2.1.0. |
| [memcached.sess\_remove\_failed](memcached.configuration.md#ini.memcached.sess-remove-failed) | On | **`INI_ALL`** | Доступно з memcached 2.1.0. Замінено на `memcached.sess_remove_failed_servers` в memcached 3.0.0. |
| [memcached.compression\_type](memcached.configuration.md#ini.memcached.compression-type) | fastlz | **`INI_ALL`** | Доступно з memcached 0.1.0. |
| [memcached.compression\_factor](memcached.configuration.md#ini.memcached.compression-factor) | 1.3 | **`INI_ALL`** | Доступно з memcached 0.1.0. |
| [memcached.compression\_threshold](memcached.configuration.md#ini.memcached.compression-threshold) | 2000 | **`INI_ALL`** | Доступно з memcached 0.1.0. |
| [memcached.serializer](memcached.configuration.md#ini.memcached.serializer) | igbinary | **`INI_ALL`** | Доступно з memcached 0.1.0. |
| [memcached.use\_sasl](memcached.configuration.md#ini.memcached.use-sasl) | Off | **`INI_SYSTEM`** | Доступно з memcached 2.2.0. Видалено в memcached 3.0.0. |
| [memcached.default\_binary\_protocol](memcached.configuration.md#ini.memcached.default-binary-protocol) | Off | **`INI_ALL`** | Доступно з memcached 3.0.0. |
| [memcached.default\_connect\_timeout](memcached.configuration.md#ini.memcached.default-connect-timeout) |  | **`INI_ALL`** | Доступно з memcached 3.0.0. |
| [memcached.default\_consistent\_hash](memcached.configuration.md#ini.memcached.default-consistent-hash) | Off | **`INI_ALL`** | Доступно з memcached 3.0.0. |
| [memcached.sess\_binary\_protocol](memcached.configuration.md#ini.memcached.sess-binary-protocol) | On | **`INI_ALL`** | Доступно з memcached 3.0.0. Замінено на `memcached.sess_binary` |
| [memcached.sess\_connect\_timeout](memcached.configuration.md#ini.memcached.sess-connect-timeout) | 1000 | **`INI_ALL`** | Доступно з memcached 2.2.0. |
| [memcached.sess\_consistent\_hash\_type](memcached.configuration.md#ini.memcached.sess-consistent-hash-type) | ketama | **`INI_ALL`** | Доступно з memcached 3.1.0. |
| [memcached.sess\_lock\_expire](memcached.configuration.md#ini.memcached.sess-lock-expire) |  | **`INI_ALL`** | Доступно з memcached 2.2.0. |
| [memcached.sess\_lock\_retries](memcached.configuration.md#ini.memcached.sess-lock-retries) | 5 | **`INI_ALL`** | Доступно з memcached 3.0.0. |
| [memcached.sess\_lock\_wait\_max](memcached.configuration.md#ini.memcached.sess-lock-wait-max) | 150 | **`INI_ALL`** | Доступно з memcached 3.0.0. Значення за замовчуванням `150` з memcached 3.1.0 (попереднє значення `2000` |
| [memcached.sess\_lock\_wait\_min](memcached.configuration.md#ini.memcached.sess-lock-wait-min) | 150 | **`INI_ALL`** | Доступно з memcached 3.0.0. Значення за замовчуванням `150` з memcached 3.1.0 (попереднє значення `1000` |
| [memcached.sess\_persistent](memcached.configuration.md#ini.memcached.sess-persistent) | Off | **`INI_ALL`** | Доступно з memcached 3.0.0. |
| [memcached.sess\_remove\_failed\_servers](memcached.configuration.md#ini.memcached.sess-remove-failed-servers) | Off | **`INI_ALL`** | Доступно з memcached 3.0.0. Замінено на `memcached.sess_remove_failed` |
| [memcached.sess\_server\_failure\_limit](memcached.configuration.md#ini.memcached.sess-server-failure-limit) |  | **`INI_ALL`** | Доступно з memcached 3.0.0. |
| [memcached.sess\_sasl\_password](memcached.configuration.md#ini.memcached.sess-sasl-password) | null | **`INI_ALL`** | Доступно з memcached 2.2.0. |
| [memcached.sess\_sasl\_username](memcached.configuration.md#ini.memcached.sess-sasl-username) | null | **`INI_ALL`** | Доступно з memcached 2.2.0. |
| [memcached.store\_retry\_count](memcached.configuration.md#ini.memcached.store-retry-count) |  | **`INI_ALL`** | Доступно з memcached 2.2.0. Значення за замовчуванням з memcached 3.2.0 (попереднє значення |

Коротке пояснення конфігураційних директив.

`memcached.sess_locking`bool

Використовувати блокування сесій. Допустимі значення: `On` `Off`По умолчанию —`On`

`memcached.sess_consistent_hash`bool

Если установлено значение`On`, то для обробки сесій буде використано узгоджене хешування (libketama). У разі використання погодженого хешування можна додавати або видаляти вузли кешування без великих втрат кешованих ключів. За замовчуванням -`On`

`memcached.sess_binary`bool

Використовувати бінарний режим сесії. Репліки модуля libmemcached працюють тільки якщо включений цей режим. За замовчуванням - `Off`

`memcached.sess_lock_wait`int

Час очікування повторної синхронізації сесії у мікросекундах. Під час встановлення цього значення потрібно бути обережним. Допустимі цілочисельні значення. Якщо встановлено значення , то буде використано значення за промовчанням. Негативні значення зменшують блокування спроб блокування. За замовчуванням - `150000`

`memcached.sess_prefix`string

Префикс ключа сессии. Строка длиной не более 219 байтов. По умолчанию —`memc.sess.key`

`memcached.sess_number_of_replicas`int

Записувати дані на ряд додаткових серверів memcached. Це "висока доступність для бідняків", як її називає модуль libmemcached. Якщо це значення позитивне та активований режим `sessions_remove_failed_servers`Коли сервер memcached виходить з ладу, сесія, як і раніше, доступна з репліки. Однак, якщо сервер memcache, що відмовив, знову стає доступним, він буде читати сесію звідти, яка може мати старі дані або взагалі не мати даних. За замовчуванням -

`memcached.sess_randomize_replica_read`bool

Випадкове читання репліки memcached сесією.

`memcached.sess_remove_failed`int

Дозволити автоматичне видалення недоступних серверів memcached.

`memcached.compression_type`string

Налаштування типу стиснення, коректні значення: `fastlz` `zlib`По умолчанию —`fastlz`

`memcached.compression_factor`float

Коефіцієнт стиснення. Зберігати значення стиснутими лише якщо коефіцієнт стиснення перевищує заданий. Зберігаємо стиснутим, якщо: `plain_len > comp_len * factor`По умолчанию —`1.3` (Економія місця 23%).

`memcached.compression_threshold`int

Поріг стиснення. Не стискати серіалізовані значення менше вказаного розміру. За замовчуванням `2000`байтов.

`memcached.serializer`string

Встановлює стандартний серіалізатор для нових об'єктів memcached. Допустимі значення: `php` `igbinary` `json` `json_array` `msgpack`

json

Стандартне для PHP кодування у форматі JSON. Цей серіалізатор швидкий і компактний, але працює тільки з даними в кодуванні UTF-8 і не повністю реалізує серіалізацію. Докладніше про це описано в описі модуля JSON. Доступно з memcached 0.2.0.

json\_array

Той же `json`але декодується в масиви. Доступно з memcached 2.0.0.

php

Стандартний серіалізатор PHP.

igbinary

Бінарний серіалізатор. Доступно з memcached 0.1.4

msgpack

Міжмовний двійковий серіалізатор. Доступно з memcached 2.2.0.

По умолчанию`igbinary`, якщо доступний, потім `igbinary`якщо доступний, інакше PHP.

`memcached.use_sasl`bool

Використовувати автентифікацію SASL під час з'єднання. Допустимі значення: `On` `Off`По умолчанию —`Off`

`memcached.default_binary_protocol`bool

Встановлює протокол memcached за промовчанням для нових підключень. (Щоб налаштувати протокол memcached для з'єднань, що використовуються сесіями, замість неї використовують директиву `memcached.sess_binary_protocol`.) Если установлено значение`On`За замовчуванням буде використано двійковий протокол memcached. Якщо встановлено значення `Off`, буде використаний текстовий протокол memcached. За замовчуванням - `Off`

`memcached.default_connect_timeout`int

Встановлює час очікування з'єднання memcached за промовчанням для нових з'єднань. (Щоб налаштувати час очікування з'єднання memcached для сесій, натомість використовують `memcached.sess_connect_timeout`.) У неблокуючому режимі це змінює значення часу очікування під час підключення до сокету в мілісекундах. Вказівка `-1` означає нескінченний час очікування. Вказівка означает использование времени ожидания соединения по умолчанию для библиотеки memcached. По умолчанию —

`memcached.default_consistent_hash`bool

Встановлює значення за промовчанням для узгодженого хешування нових підключень. (Щоб налаштувати узгоджене хешування для сесій, натомість використовують `memcached.sess_consistent_hash`.) Если установлено значение`On`Для обробки сесії використовується узгоджене хешування (libketama). Коли використовується узгоджене хешування, можна додавати або видаляти вузли кеша, не турбуючись про те, що ключі за замовчуванням відключені.

`memcached.sess_binary_protocol`bool

Використовувати двійковий протокол memcached для сесій memcached (замість текстового протоколу). Репліки модуля libmemcached працюють, тільки якщо включено двійковий режим. Однак деякі проксі (наприклад, twemproxy) працюватимуть, лише якщо двійковий протокол вимкнено. За замовчуванням -`On` з libmemcached 1.0.18 або більше. До libmemcached 1.0.18 значення за промовчанням `Off`

> **Зауваження**: У більш старих версіях php-memcached ця директива була вимкнена і називалася `memcached.sess_binary`

`memcached.sess_connect_timeout`int

Значення часу очікування з'єднання memcached. У неблокувальному режимі це змінює значення часу очікування під час з'єднання сокету в мілісекундах. Вказівка `-1` означає нескінченний час очікування.

`memcached.sess_consistent_hash_type`string

Тип согласованного хеширования сессии Memcached. Если установлено значение`ketama`(по умолчанию для php-memcached 3.x), для обработки сессии используется согласованное хеширование модуля libketama, если установлено значение`ketama_weighted` (за промовчанням для php-memcached 2.x), для обробки сесії використовується зважене узгоджене хешування (модуль libketama). За замовчуванням - `ketama`

`memcached.sess_lock_expire`int

Час у секундах до того, як має спрацювати блокування. Встановлення значення приводит к поведению по умолчанию — будет использована PHP-директива`max_execution_time`По умолчанию —

`memcached.sess_lock_retries`int

Кількість спроб повторного блокування сесії, не включаючи першу спробу. За замовчуванням - `5`

`memcached.sess_lock_wait_max`int

Максимальний час очікування у мілісекундах між спробами блокування сесії. За замовчуванням - `150`

`memcached.sess_lock_wait_min`int

Мінімальний час очікування у мілісекундах між спробами блокування сесії. Це значення подвоюється при кожній спробі блокування, доки не буде досягнуто значення, задане директивою `memcached.sess_lock_wait_max`, чергові спроби займатимуть час досягнутого значення. За замовчуванням - `150`

`memcached.sess_persistent`bool

Чи слід повторно використовувати з'єднання memcached, що відповідають значенню (значенням) директиви `session.save_path` після завершення виконання сценарію. Цю директиву не використовують, якщо певні налаштування (наприклад, SASL, sess\_binary\_protocol) будуть перевизначені між запитами. За замовчуванням - `Off`

`memcached.sess_remove_failed_servers`bool

Дозволити автоматичне видалення сервера, що відмовив, memcached. За замовчуванням - `Off`

> **Зауваження**: У попередніх версіях ця директива називалася `memcached.sess_remove_failed`

`memcached.sess_server_failure_limit`int

Встановлення більшого, ніж встановлене за умовчанням, значення дозволить видалення сервера після заданої кількості безперервних збоїв підключення. За замовчуванням -

`memcached.sess_sasl_password`string

Пароль сесії SASL. Для включення SASL необхідно вказати ім'я користувача та пароль.

`memcached.sess_sasl_username`string

Ім'я користувача SASL. Для включення SASL необхідно вказати ім'я користувача та пароль.

`memcached.store_retry_count`int

Кількість повторних спроб невдалих команд збереження. Цей механізм прозоро перемикає на вторинні сервери при збої операцій set/increment/decrement/setMulti на бажаному сервері серед безлічі серверів. За замовчуванням -
