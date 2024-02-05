---
navigation:
  - yaf.tutorials.md: « Приклади
  - class.yaf-application.md: Yaf\_Application »
  - index.md: PHP Manual
  - book.yaf.md: Yaf
title: Конфігурація програми
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Конфігурація програми

Ви повинні встановити конфігурацію у вигляді масиву або INI файлу (Дивіться [Yaf\_Config\_Ini](class.yaf-config-ini.md)) у конструкторі [Yaf\_Application::\_\_construct()](yaf-application.construct.md)

Yaf автоматично об'єднає параметри програми та настройки користувача. Конфігурація додатків має префікс "yaf." або "application.". Якщо вказано обидва "yaf." та "application.", перевага буде віддана "application.".

**Приклад #1 Приклад PHP масиву**

```php
<?php
    $configs = array(
            "application" => array(
                "directory" => dirname(__FILE__),
                "dispatcher" => array(
                      "catchException" => 0,
                    ),
                "view" => array(
                       "ext" => "phtml",
                    ),
                ),
           );
    $app = new Yaf_Application($config);
?>
```

**Приклад #2 Приклад файлу INI**

\[yaf\]yaf.directory = APPLICATION\_PATH "/appliation" yaf.dispatcher.catchException = 0

\[product : yaf\]; user configuration list here

**Конфігурація Yaf програми**

| Имя | По умолчанию | Список изменений |
| --- | --- | --- |
| application.directory |  |  |
| application.ext | "php" |  |
| application.view.ext | "phtml" |  |
| application.modules | "index" |  |
| application.library | application.directory . "/library" |  |
| application.library.directory | application.directory . "/library" |  |
| application.library.namespace | "" |  |
| application.bootstrap | application.directory . "/Bootstrap" . application.ext |  |
| application.baseUri | "" |  |
| application.dispatcher.defaultRoute |  |  |
| application.dispatcher.throwException |  |  |
| application.dispatcher.catchException |  |  |
| application.dispatcher.defaultModule | "index" |  |
| application.dispatcher.defaultController | "index" |  |
| application.dispatcher.defaultAction | "index" |  |
| application.system |  |  |

Коротке пояснення конфігураційних директив.

`application.directory`string

Директорія, яка містить папки "controllers" (контролери), "views" (шаблони виведення), "models" (моделі), "plugins" (плагіни).

> **Зауваження** :
> 
> Це єдина конфігурація, яка не має параметрів за замовчуванням. Ви повинні ввести її вручну.

`application.ext`string

Розширення файлів PHP-скриптів, що використовуються в класі автозавантаження ( [Yaf\_Loader](class.yaf-loader.md)

`application.view.ext`string

Розширення файлів шаблонів виводу.

`application.modules`string

Список зареєстрованих модулів, розділених комами, що використовуються в маршрутизації, особливо якщо в PATH\_INFO більше трьох сегментів,

Yaf повинен мати можливість зрозуміти, чи є перший сегмент ім'ям модуля чи ні.

`application.library`string

Локальний каталог з бібліотеками, дивіться [Yaf\_Loader](class.yaf-loader.md) і [yaf.library](yaf.configuration.md#ini.yaf.library)

> **Зауваження** :
> 
> Після Yaf 2.1.6, ця настройка повинна являти собою масив. Шлях до бібліотек намагатиметься використовувати елементи [application.library.directory](yaf.appconfig.md#configuration.yaf.library.directory)

`application.library.directory`string

Псевдоним для[application.library](yaf.appconfig.md#configuration.yaf.library)Добавлено в Yaf 2.1.6

`application.library.namespace`string

Префікси просторів імен локальних бібліотек, перераховані через кому.

Додано в Yaf 2.1.6

`application.bootstrap`string

Абсолютний шлях до скрипта класу Bootstrap.

`application.baseUri`string

Використовується для видалення фіксованого префікса запиту URI в процесі маршрутизації. Наприклад, надійшов запит до "/prefix/controller/action". Якщо ви поставите application.baseUri рівним "/prefix", то в процесі маршрутизації, як PATH\_INFO використовуватиметься лише "/controller/action".

Загалом, це досить марна настройка.

`application.dispatcher.throwException`bool

Якщо встановлено як On, Yaf викидатиме винятки у разі виникнення помилок. Також дивіться [Yaf\_Dispatcher::throwException()](yaf-dispatcher.throwexception.md)

`application.dispatcher.catchException`bool

Якщо встановлено як On, Yaf надсилатиме не оброблені винятки в контролер Помилок/Дій. Також дивіться [Yaf\_Dispatcher::catchException()](yaf-dispatcher.catchexception.md)

`application.dispatcher.defaultRoute`string

Маршрутизация по умолчанию, если не задано, то, по умолчанию, будет использован маршрут Static. Смотрите:[Yaf\_Router::addRoute()](yaf-router.addroute.md)

`application.dispatcher.defaultModule`string

Имя модуля по умолчанию, также смотрите[Yaf\_Dispatcher::setDefaultModule()](yaf-dispatcher.setdefaultmodule.md)

`application.dispatcher.defaultController`string

Имя контроллера по умолчанию, также смотрите[Yaf\_Dispatcher::setDefaultController()](yaf-dispatcher.setdefaultcontroller.md)

`application.dispatcher.defaultAction`string

Имя действия по умолчанию, также смотрите[Yaf\_Dispatcher::setDefaultAction()](yaf-dispatcher.setdefaultaction.md)

`application.system`string

Устанавливает конфигурацию времени исполнения yaf в application.ini, типа:[application.system.lowcase\_path](yaf.configuration.md#ini.yaf.lowcase-path)

> **Зауваження** :
> 
> тільки **`INI_ALL`** опції можуть бути встановлені таким чином
