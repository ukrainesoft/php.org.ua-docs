---
navigation:
  - memcache.installation.md: « Встановлення
  - memcache.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - memcache.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні параметри Memcache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [memcache.allow\_failover](memcache.ini.md#ini.memcache.allow-failover) | "1" | **`INI_ALL`** | Доступно з memcache 2.0.2. |
| [memcache.max\_failover\_attempts](memcache.ini.md#ini.memcache.max-failover-attempts) | "20" | **`INI_ALL`** | Доступно з memcache 2.1.0. |
| [memcache.chunk\_size](memcache.ini.md#ini.memcache.chunk-size) | "8192" | **`INI_ALL`** | Доступно з memcache 2.0.2. |
| [memcache.default\_port](memcache.ini.md#ini.memcache.default-port) | "11211" | **`INI_ALL`** | Доступно з memcache 2.0.2. |
| [memcache.hash\_strategy](memcache.ini.md#ini.memcache.hash-strategy) | "standard" | **`INI_ALL`** | Доступно з memcache 2.2.0. |
| [memcache.hash\_function](memcache.ini.md#ini.memcache.hash-function) | "crc32" | **`INI_ALL`** | Доступно з memcache 2.2.0. |
| [memcache.protocol](memcache.ini.md#ini.memcache.protocol) | ascii | **`INI_ALL`** | Підтримується з memcache 3.0.0 |
| [memcache.redundancy](memcache.ini.md#ini.memcache.redundancy) |  | **`INI_ALL`** | Підтримується з memcache 3.0.0 |
| [memcache.session\_redundancy](memcache.ini.md#ini.memcache.session-redundancy) |  | **`INI_ALL`** | Підтримується з memcache 3.0.0 |
| [memcache.compress\_threshold](memcache.ini.md#ini.memcache.compress-threshold) | 20000 | **`INI_ALL`** | Підтримується з memcache 3.0.3 |
| [memcache.lock\_timeout](memcache.ini.md#ini.memcache.lock-timeout) | 15 | **`INI_ALL`** | Підтримується з memcache 3.0.4 |

**Параметри конфігурації сесії, що впливають на поведінку Memcache**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [session.save\_handler](memcache.ini.md#ini.memcache.save-handler) | "files" | **`INI_ALL`** | Підтримується, починаючи з memcache 2.1.2 |
| [session.save\_path](memcache.ini.md#ini.memcache.save-path) | "" | **`INI_ALL`** | Підтримується, починаючи з memcache 2.1.2 |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`memcache.allow_failover`bool

Дозвіл прозорого перемикання (failover) на інші сервери у разі виникнення помилок.

`memcache.max_failover_attempts`int

Встановлює кількість спроб читання та запису даних. Використовується лише у поєднанні з memcache.allow\_failover.

`memcache.chunk_size`int

Встановлює розмір блоків даних, що передаються. Використання малих значень призводить до підвищення активності мережі. У разі несподіваного уповільнення роботи, спробуйте збільшити значення до 32768.

`memcache.default_port`string

Встановлює номер порту TCP за замовчуванням для підключення до сервера memcached, якщо явно не вказано інший.

`memcache.hash_strategy`string

Контролює стратегію функцій відображення ключів на сервері. Встановіть цей параметр у `consistent` для включення послідовного хешування, яке не вимагає перепризначення ключів кешу при додаванні та видаленні серверів з пулу. Встановлення цього параметра в `standard` призводить до використання стару стратегію.

`memcache.hash_function`string

Устанавливает хеш-функцию для отображения ключей на сервера. При значении`crc32` буде використовуватися стандартний CRC32 хеш, а при `fnv`\- FNV-1a.

`memcache.protocol`string

`memcache.redundancy`int

`memcache.session_redundancy`int

`memcache.compress_threshold`int

`memcache.lock_timeout`int

`session.save_handler`string

Встановіть цей параметр у `memcache`для использования memcache в качестве обработчика сессий.

`session.save_path`string

Встановлює список адрес серверів, розділених комою, для зберігання сесій. Наприклад, `"tcp://host1:11211, tcp://host2:11211"`

Кожна адреса може містити параметри, аналогічні використовуваним методом [Memcache::addServer()](memcache.addserver.md), які будуть використані сервером. Наприклад, `"tcp://host1:11211?persistent=1&weight=1&timeout=1&retry_interval=15"`
