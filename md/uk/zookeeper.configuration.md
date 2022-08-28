Налаштування під час виконання

-   [« Установка](zookeeper.installation.html)
    
-   [Типы ресурсов »](zookeeper.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](zookeeper.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Zookeeper**

| Имя                                                                                     | По умолчанию | Место изменения | История изменений |
|-----------------------------------------------------------------------------------------|--------------|-----------------|-------------------|
| [zookeeper.recv\_timeout](zookeeper.configuration.html#ini.zookeeper.recv_timeout)      |              | PHPINIALL       |                   |
| [zookeeper.session\_lock](zookeeper.configuration.html#ini.zookeeper.session_lock)      |              | PHPINISYSTEM    |                   |
| [zookeeper.sess\_lock\_wait](zookeeper.configuration.html#ini.zookeeper.sess_lock_wait) |              | PHPINIALL       |                   |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`zookeeper.recv_timeout` int

Час очікування за промовчанням для всіх сесій ZooKeeper.

`zookeeper.session_lock` int

Дозволяє блокування сесій PHP.

`zookeeper.sess_lock_wait` int

Час очікування повтору при взаємному блокуванні сесії PHP у мікросекундах. Будьте обережні, встановлюючи це значення. Коректні значення - цілі числа, що за замовчуванням використовуються 0. Негативні значення призводить до зменшення спроб блокування.