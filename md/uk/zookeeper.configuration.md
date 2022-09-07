---
navigation:
  - zookeeper.installation.md: « Установка
  - zookeeper.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - zookeeper.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Zookeeper**

| Имя | По умолчанию | Место изменения | История изменений |
| --- | --- | --- | --- |
| [zookeeper.recvtimeout](zookeeper.configuration.md#ini.zookeeper.recv_timeout) |  | PHPINIALL |  |
| [zookeeper.sessionlock](zookeeper.configuration.md#ini.zookeeper.session_lock) |  | PHPINISYSTEM |  |
| [zookeeper.sesslockwait](zookeeper.configuration.md#ini.zookeeper.sess_lock_wait) |  | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`zookeeper.recv_timeout` int

Час очікування за промовчанням для всіх сесій ZooKeeper.

`zookeeper.session_lock` int

Дозволяє блокування сесій PHP.

`zookeeper.sess_lock_wait` int

Час очікування повтору при взаємному блокуванні сесії PHP у мікросекундах. Будьте обережні, встановлюючи це значення. Коректні значення - цілі числа, що за замовчуванням використовуються 0. Негативні значення призводить до зменшення спроб блокування.
