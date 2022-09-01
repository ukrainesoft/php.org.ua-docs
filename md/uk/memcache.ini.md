---
navigation:
  - memcache.installation.md: « Установка
  - memcache.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - memcache.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні параметри Memcache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [memcache.allowfailover](memcache.ini.html#ini.memcache.allow-failover) | "1" | PHPINIALL | Доступно з memcache 2.0.2. |
| [memcache.maxfailoverattempts](memcache.ini.html#ini.memcache.max-failover-attempts) | "20" | PHPINIALL | Доступно з memcache 2.1.0. |
| [memcache.chunksize](memcache.ini.html#ini.memcache.chunk-size) | "8192" | PHPINIALL | Доступно з memcache 2.0.2. |
| [memcache.defaultport](memcache.ini.html#ini.memcache.default-port) | "11211" | PHPINIALL | Доступно з memcache 2.0.2. |
| [memcache.hashstrategy](memcache.ini.html#ini.memcache.hash-strategy) | "standard" | PHPINIALL | Доступно з memcache 2.2.0. |
| [memcache.hashfunction](memcache.ini.html#ini.memcache.hash-function) | "crc32" | PHPINIALL | Доступно з memcache 2.2.0. |
| [memcache.protocol](memcache.ini.html#ini.memcache.protocol) | ascii | \>PHPINIALL | Підтримується з memcache 3.0.0 |
| [memcache.redundancy](memcache.ini.html#ini.memcache.redundancy) |  | \>PHPINIALL | Підтримується з memcache 3.0.0 |
| [memcache.sessionredundancy](memcache.ini.html#ini.memcache.session-redundancy) |  | \>PHPINIALL | Підтримується з memcache 3.0.0 |
| [memcache.compressthreshold](memcache.ini.html#ini.memcache.compress-threshold) |  | \>PHPINIALL | Підтримується з memcache 3.0.3 |
| [memcache.locktimeout](memcache.ini.html#ini.memcache.lock-timeout) |  | \>PHPINIALL | Підтримується з memcache 3.0.4 |

**Параметри конфігурації сесії, що впливають на поведінку Memcache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [session.savehandler](memcache.ini.html#ini.memcache.save-handler) | "files" | PHPINIALL | Підтримується, починаючи з memcache 2.1.2 |
| [session.savepath](memcache.ini.html#ini.memcache.save-path) | "" | PHPINIALL | Підтримується, починаючи з memcache 2.1.2 |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`memcache.allow_failover` bool

Дозвіл прозорого перемикання на інші сервери при виникненні помилок.

`memcache.max_failover_attempts` int

Встановлює кількість спроб читання та запису даних. Використовується лише у поєднанні з memcache.allowfailover.

`memcache.chunk_size` int

Встановлює розмір блоків даних, що передаються. Використання малих значень призводить до підвищення активності мережі. У разі несподіваного уповільнення роботи, спробуйте збільшити значення до 32768.

`memcache.default_port` string

Встановлює номер порту TCP за замовчуванням для підключення до сервера memcached, якщо явно не вказано інший.

`memcache.hash_strategy` string

Контролює стратегію функцій відображення ключів на сервері. Встановіть цей параметр у `consistent` для включення послідовного хешування, яке не вимагає перепризначення ключів кешу при додаванні та видаленні серверів з пулу. Встановлення цього параметра в `standard` призводить до використання стару стратегію.

`memcache.hash_function` string

Встановлює хеш-функцію для відображення ключів на сервері. При значенні `crc32` буде використовуватися стандартний CRC32 хеш, а при `fnv` - FNV-1a.

`memcache.protocol` string

`memcache.redundancy` int

`memcache.session_redundancy` int

`memcache.compress_threshold` int

`memcache.lock_timeout` int

`session.save_handler` string

Встановіть цей параметр у `memcache` для використання memcache як оброблювач сесій.

`session.save_path` string

Встановлює список адрес серверів, розділених комою, для зберігання сесій. Наприклад, `"tcp://host1:11211, tcp://host2:11211"`

Кожна адреса може містити параметри, аналогічні використовуваним методом [Memcache::addServer()](memcache.addserver.md), які будуть використані сервером. Наприклад, `"tcp://host1:11211?persistent=1&weight=1&timeout=1&retry_interval=15"`
