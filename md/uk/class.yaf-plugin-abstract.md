Клас YafPluginAbstract

-   [« Yaf\_Loader::setLibraryPath](yaf-loader.setlibrarypath.html)
    
-   [Yaf\_Plugin\_Abstract::dispatchLoopShutdown »](yaf-plugin-abstract.dispatchloopshutdown.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafPluginAbstract
    

# Клас YafPluginAbstract

(Yaf >=1.0.0)

## Вступ

Плагіни дозволяють легко розширювати та налаштовувати фреймворк.

Плагіни є класами. Визначення класу змінюватиметься в залежності від компонента - вам може знадобитися реалізувати цей інтерфейс, але факт залишається фактом, плагін сам є класом.

Плагін повинен бути завантажений у Yaf з використанням [Yaf\_Dispatcher::registerPlugin()](yaf-dispatcher.registerplugin.html). Після реєстрації всі методи, реалізовані плагіном відповідно до цього інтерфейсу, будуть викликатися вчасно.

## Приклади

**Приклад #1 Приклад плагіна**

```php
<?php
   /* Класс bootstrap должен быть определён как ./application/Bootstrap.php */
   class Bootstrap extends Yaf_Bootstrap_Abstract {
        public function _initPlugin(Yaf_Dispatcher $dispatcher) {
            /* регистрируем плагин */
            $dispatcher->registerPlugin(new TestPlugin());
        }
   }

   /* класс плагина должен лежать в ./application/plugins/ */
   class TestPlugin extends Yaf_Plugin_Abstract {
        public function routerStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            /* перед тем, как приступит к работе маршрутизатор,
                пользователь может сам поработать с перезаписью URL */
            var_dump("routerStartup");
        }
        public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            /* Маршрутизатор отработал, следовательно можно перейти к проверке логина */
            var_dump("routerShutdown");
        }
        public function dispatchLoopStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            var_dump("dispatchLoopStartup");
        }
        public function preDispatch(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            var_dump("preDispatch");
        }
        public function postDispatch(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            var_dump("postDispatch");
        }
        public function dispatchLoopShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
            /* последняя возможность для пользователя что-то сделать */
            var_dump("dispatchLoopShutdown");
        }
   }

   Class IndexController extends Yaf_Controller_Abstract {
        public function indexAction() {
            return FALSE; //предотвращаем рендеринг
        }
   }

   $config = array(
       "application" => array(
           "directory" => dirname(__FILE__) . "/application/",
       ),
   );

   $app = new Yaf_Application($config);
   $app->bootstrap()->run();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(13) "routerStartup"
string(14) "routerShutdown"
string(19) "dispatchLoopStartup"
string(11) "preDispatch"
string(12) "postDispatch"
string(20) "dispatchLoopShutdown"
```

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Plugin_Abstract
     
     {
    

    /* Методы */
    
   public dispatchLoopShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
public dispatchLoopStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
public postDispatch(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
public preDispatch(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
public preResponse(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
public routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
public routerStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void

   }
```

## Зміст

-   [Yaf\_Plugin\_Abstract::dispatchLoopShutdown](yaf-plugin-abstract.dispatchloopshutdown.html) — Призначення dispatchLoopShutdown
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup](yaf-plugin-abstract.dispatchloopstartup.html) - Хук перед відправкою циклу
-   [Yaf\_Plugin\_Abstract::postDispatch](yaf-plugin-abstract.postdispatch.html) - Призначення postDispatch
-   [Yaf\_Plugin\_Abstract::preDispatch](yaf-plugin-abstract.predispatch.html) - Призначення preDispatch
-   [Yaf\_Plugin\_Abstract::preResponse](yaf-plugin-abstract.preresponse.html) - Призначення preResponse
-   [Yaf\_Plugin\_Abstract::routerShutdown](yaf-plugin-abstract.routershutdown.html) - Призначення routerShutdown
-   [Yaf\_Plugin\_Abstract::routerStartup](yaf-plugin-abstract.routerstartup.html) - Перехоплювач RouterStartup