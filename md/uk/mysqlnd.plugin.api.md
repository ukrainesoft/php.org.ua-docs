---
navigation:
  - mysqlnd.plugin.architecture.md: « Архітектура плагінів MySQL Native Driver
  - mysqlnd.plugin.developing.md: Розпочинаємо розробку плагіна mysqlnd »
  - index.md: PHP Manual
  - mysqlnd.plugin.md: API для плагінів до вбудованого драйвера MySQL
title: API плагінів mysqlnd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## API плагінів mysqlnd

API плагінів `mysqlnd`предоставляет следующие функции:

-   mysqlnd\_plugin\_register()
    
-   mysqlnd\_plugin\_count()
    
-   mysqlnd\_plugin\_get\_plugin\_connection\_data()
    
-   mysqlnd\_plugin\_get\_plugin\_result\_data()
    
-   mysqlnd\_plugin\_get\_plugin\_stmt\_data()
    
-   mysqlnd\_plugin\_get\_plugin\_net\_data()
    
-   mysqlnd\_plugin\_get\_plugin\_protocol\_data()
    
-   mysqlnd\_conn\_get\_methods()
    
-   mysqlnd\_result\_get\_methods()
    
-   mysqlnd\_result\_meta\_get\_methods()
    
-   mysqlnd\_stmt\_get\_methods()
    
-   mysqlnd\_net\_get\_methods()
    
-   mysqlnd\_protocol\_get\_methods()
    

Немає стандартних визначень того, що таке плагін та як він працює.

Часто зустрічаються в плагінах компоненти:

-   Менеджер плагіна
    
-   API плагіна
    
-   Сервіси програми (або модулі)
    
-   API сервісів програми (або API модулів)
    

Концепция плагина`mysqlnd` експлуатує цю функціональність і, крім того, тішить нас відкритою архітектурою.

**Немає заборон**

Плагін має повний доступ до всіх нутрощів. `mysqlnd`. Немає обмежень або заборон, пов'язаних із безпекою. Все, що завгодно, можна переписати для реалізації дружніх або ворожих алгоритмів, так що рекомендується ставити плагіни тільки з довірених джерел.

Як обговорювалося вище, плагіни можуть вільно використовувати покажчики. Ці покажчики нічим не обмежені і можуть вказувати дані іншого плагіна. Найпростіша арифметична операція дозволить отримати доступ до даних іншого плагіна.

Рекомендується писати плагіни, що співпрацюють, які можуть працювати спільно з іншими плагінами і завжди викликати батьківські методи. Плагіни ніколи не повинні поводитися вороже до самого `mysqlnd`

**Проблеми: приклад співробітництва та побудови ланцюжка**

| Модуль | Указатель mysqlnd.query() | Стек вызова, если вызывается родитель |
| --- | --- | --- |
| ext/mysqlnd | mysqlnd.query() | mysqlnd.query |
| ext/mysqlnd\_cache | mysqlnd\_cache.query() |  |

1.  mysqlnd\_cache.query()
    
2.  mysqlnd.query
    

| | ext/mysqlnd\_monitor | mysqlnd\_monitor.query() |

1.  mysqlnd\_monitor.query()
    
2.  mysqlnd\_cache.query()
    
3.  mysqlnd.query
    

У цьому сценарії завантажені плагіни кеша (`ext/mysqlnd_cache`) та моніторингу (`ext/mysqlnd_monitor`). Оба наследуют класс`Connection::query()`. реєстрація плагінів відбувається на етапі `MINIT` відповідно до описаної вище логіки. PHP за замовчуванням викликає модулі в алфавітному порядку. Плагіни не знають один про одного і не накладають будь-яких залежностей.

За умовчанням, плагіни викликають батьківський метод query зі своєї, перевизначеної, версії цього методу.

**Резюме з модуля PHP**

Повторення пройденого матеріалу на прикладі поведінки плагіна `ext/mysqlnd_plugin`, що використовує API плагінів `mysqlnd`для PHP:

-   Будь-яка програма PHP, що використовує MySQL намагається встановити з'єднання за адресою 192.168.2.29
    
-   Додаток використовує один із наступних модулів`ext/mysql` `ext/mysqli`или`PDO_MYSQL`. Усі три модулі використовують`mysqlnd`для з'єднання з 192.168.2.29.
    
-   `Mysqlnd`викликає метод з'єднання, який успадковується плагіном`ext/mysqlnd_plugin`
    
-   `ext/mysqlnd_plugin`викликає зареєстрований користувачем метод`proxy::connect()`
    
-   Цей метод підміняє IP адресу з'єднання з 192.168.2.29 на 127.0.0.1 та повертає встановлене`parent::connect()`соединение.
    
-   `ext/mysqlnd_plugin`робить те саме, що і`parent::connect(127.0.0.1)`викликаючи оригінальний метод`mysqlnd`для соединения.
    
-   `ext/mysqlnd`встановлює з'єднання та повертає його`ext/mysqlnd_plugin`. . `ext/mysqlnd_plugin`, своєю чергою, передає його далі.
    
-   Не має значення, який модуль був використаний, він все одно отримає з'єднання до 127.0.0.1. Після цього модуль повертає це з'єднання додатку. Коло замкнулося.
