Конфігурація програми

-   [« Примеры](yaf.tutorials.html)
    
-   [Yaf\_Application »](class.yaf-application.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Конфігурація програми
    

# Конфігурація програми

Ви повинні встановити конфігурацію у вигляді масиву або INI файлу (Дивіться [Yaf\_Config\_Ini](class.yaf-config-ini.html)) у конструкторі [Yaf\_Application::\_\_construct()](yaf-application.construct.html)

Yaf автоматично об'єднає параметри програми та настройки користувача. Конфігурація додатків має префікс "yaf." або "application.". Якщо вказано обидва "yaf." та "application.", перевага буде віддана "application.".

**Приклад #1 Приклад PHP масиву**

```php
<?php
    $configs = array(
            "application" => array(
                "directory" => dirname(__FILE__),
                "dispatcher" => array(
                      "catchException" => 0,
                    ),
                "view" => array(
                       "ext" => "phtml",
                    ),
                ),
           );
    $app = new Yaf_Application($config);
?>
```

**Приклад #2 Приклад файлу INI**

yafyaf.directory = APPLICATIONPATH "/appliation" yaf.dispatcher.catchException = 0

product : yaf; user configuration list here

**Конфігурація Yaf програми**

| Имя                                      | По умолчанию                                          | Список изменений |
|------------------------------------------|-------------------------------------------------------|------------------|
| аплікатион.директорій                    |                                                       |                  |
| application.ext                          | "php"                                                 |                  |
| application.view.ext                     | "phtml"                                               |                  |
| application.modules                      | "index"                                               |                  |
| application.library                      | application.directory. "/library"                     |                  |
| аплікатион.лібрарі.директорій            | application.directory. "/library"                     |                  |
| application.library.namespace            | ""                                                    |                  |
| application.bootstrap                    | application.directory. "/Bootstrap" . application.ext |                  |
| application.baseUri                      | ""                                                    |                  |
| application.dispatcher.defaultRoute      |                                                       |                  |
| application.dispatcher.throwException    |                                                       |                  |
| application.dispatcher.catchException    |                                                       |                  |
| application.dispatcher.defaultModule     | "index"                                               |                  |
| application.dispatcher.defaultController | "index"                                               |                  |
| application.dispatcher.defaultAction     | "index"                                               |                  |
| application.system                       |                                                       |                  |

Коротке пояснення конфігураційних директив.

`application.directory` string

Директорія, яка містить папки "controllers" (контролери), "views" (шаблони виведення), "models" (моделі), "plugins" (плагіни).

> **Зауваження**
> 
> Це єдина конфігурація, яка не має параметрів за замовчуванням. Ви повинні ввести її вручну.

`application.ext` string

Розширення файлів PHP-скриптів, що використовуються в класі автозавантаження ( [Yaf\_Loader](class.yaf-loader.html)

`application.view.ext` string

Розширення файлів шаблонів виводу.

`application.modules` string

Список зареєстрованих модулів, розділених комами, що використовуються в маршрутизації, особливо якщо в PATHINFO більше трьох сегментів,

Yaf повинен мати можливість зрозуміти, чи є перший сегмент ім'ям модуля чи ні.

`application.library` string

Локальний каталог з бібліотеками, дивіться [Yaf\_Loader](class.yaf-loader.html) і [yaf.library](yaf.configuration.html#ini.yaf.library)

> **Зауваження**
> 
> Після Yaf 2.1.6, ця настройка повинна являти собою масив. Шлях до бібліотек намагатиметься використовувати елементи [application.library.directory](yaf.appconfig.html#configuration.yaf.library.directory)

`application.library.directory` string

Псевдонім для [application.library](yaf.appconfig.html#configuration.yaf.library). Додано в Yaf 2.1.6

`application.library.namespace` string

Префікси просторів імен локальних бібліотек, перераховані через кому.

Додано в Yaf 2.1.6

`application.bootstrap` string

Абсолютний шлях до скрипта класу Bootstrap.

`application.baseUri` string

Використовується для видалення фіксованого префікса запиту URI в процесі маршрутизації. Наприклад, надійшов запит до "/prefix/controller/action". Якщо ви поставите application.baseUri рівним "/prefix", то в процесі маршрутизації, як PATHINFO використовуватиметься лише "/controller/action".

Загалом, це досить марна настройка.

`application.dispatcher.throwException` bool

Якщо встановлено як On, Yaf викидатиме винятки у разі виникнення помилок. Також дивіться [Yaf\_Dispatcher::throwException()](yaf-dispatcher.throwexception.html)

`application.dispatcher.catchException` bool

Якщо встановлено як On, Yaf надсилатиме не оброблені винятки в контролер Помилок/Дій. Також дивіться [Yaf\_Dispatcher::catchException()](yaf-dispatcher.catchexception.html)

`application.dispatcher.defaultRoute` string

Маршрутизація за замовчуванням, якщо не задано, то за промовчанням буде використаний маршрут Static. Дивіться: [Yaf\_Router::addRoute()](yaf-router.addroute.html)

`application.dispatcher.defaultModule` string

Ім'я модуля за замовчуванням також дивіться [Yaf\_Dispatcher::setDefaultModule()](yaf-dispatcher.setdefaultmodule.html)

`application.dispatcher.defaultController` string

Ім'я контролера за замовчуванням, також дивіться [Yaf\_Dispatcher::setDefaultController()](yaf-dispatcher.setdefaultcontroller.html)

`application.dispatcher.defaultAction` string

Ім'я дії за замовчуванням також дивіться [Yaf\_Dispatcher::setDefaultAction()](yaf-dispatcher.setdefaultaction.html)

`application.system` string

Встановлює конфігурацію часу виконання yaf в application.ini типу: [application.system.lowcase\_path](yaf.configuration.html#ini.yaf.lowcase-path)

> **Зауваження**
> 
> тільки PHPINIALL опції можуть бути встановлені таким чином