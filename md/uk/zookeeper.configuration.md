---
navigation:
  - zookeeper.installation.md: « Встановлення
  - zookeeper.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - zookeeper.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Zookeeper**

| Имя | По умолчанию | Место изменения | История изменений |
| --- | --- | --- | --- |
| [zookeeper.recv\_timeout](zookeeper.configuration.md#ini.zookeeper.recv_timeout) | 10000 | **`INI_ALL`** |  |
| [zookeeper.session\_lock](zookeeper.configuration.md#ini.zookeeper.session_lock) |  | **`INI_SYSTEM`** |  |
| [zookeeper.sess\_lock\_wait](zookeeper.configuration.md#ini.zookeeper.sess_lock_wait) | 150000 | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`zookeeper.recv_timeout`int

Час очікування за промовчанням для всіх сесій ZooKeeper.

`zookeeper.session_lock`int

Дозволяє блокування сесій PHP.

`zookeeper.sess_lock_wait`int

Час очікування повтору при взаємному блокуванні сесії PHP у мікросекундах. Будьте обережні, встановлюючи це значення. Коректні значення - цілі числа, що за замовчуванням використовуються 0. Негативні значення призводить до зменшення спроб блокування.
