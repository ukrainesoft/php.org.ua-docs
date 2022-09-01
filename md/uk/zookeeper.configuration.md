---
navigation:
  - zookeeper.installation.html: « Установка
  - zookeeper.resources.html: Типи ресурсів »
  - index.html: PHP Manual
  - zookeeper.setup.html: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Zookeeper**

| Имя | По умолчанию | Место изменения | История изменений |
| --- | --- | --- | --- |
| [zookeeper.recvtimeout](zookeeper.configuration.html#ini.zookeeper.recv_timeout) |  | PHPINIALL |  |
| [zookeeper.sessionlock](zookeeper.configuration.html#ini.zookeeper.session_lock) |  | PHPINISYSTEM |  |
| [zookeeper.sesslockwait](zookeeper.configuration.html#ini.zookeeper.sess_lock_wait) |  | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`zookeeper.recv_timeout` int

Час очікування за промовчанням для всіх сесій ZooKeeper.

`zookeeper.session_lock` int

Дозволяє блокування сесій PHP.

`zookeeper.sess_lock_wait` int

Час очікування повтору при взаємному блокуванні сесії PHP у мікросекундах. Будьте обережні, встановлюючи це значення. Коректні значення - цілі числа, що за замовчуванням використовуються 0. Негативні значення призводить до зменшення спроб блокування.
