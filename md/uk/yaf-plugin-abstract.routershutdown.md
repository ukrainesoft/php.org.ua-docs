Призначення routerShutdown

-   [« YafPluginAbstract::preResponse](yaf-plugin-abstract.preresponse.html)
    
-   [YafPluginAbstract::routerStartup »](yaf-plugin-abstract.routerstartup.html)
    
-   [PHP Manual](index.html)
    
-   [YafPluginAbstract](class.yaf-plugin-abstract.html)
    
-   Призначення routerShutdown
    

# YafPluginAbstract::routerShutdown

(Yaf >=1.0.0)

YafPluginAbstract::routerShutdown — Призначення routerShutdown

### Опис

```methodsynopsis
public Yaf_Plugin_Abstract::routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
```

Цей перехоплювач буде запущений після завершення процесу маршрутизації, який зазвичай використовується для перевірки входу в систему.

### Список параметрів

`request`

`response`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafPluginAbstract::routerShutdown()****

```php
<?php
class UserInitPlugin extends Yaf_Plugin_Abstract {

    public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
        $controller = $request->getControllerName();

        /**
         * Использовать контроллер доступа не нужно для API
         */
        if (in_array(strtolower($controller), array(
            'api',
        ))) {
            return TRUE;
        }

        if (Yaf_Session::getInstance()->has("login")) {
            return TRUE;
        }

        /* Ошибка проверки доступа, необходимо войти */
        $response->setRedirect("http://yourdomain.com/login/");
        return FALSE;
    }
}
?>
```

### Дивіться також

-   [YafPluginAbstract::routerStartup()](yaf-plugin-abstract.routerstartup.html) - Перехоплювач RouterStartup
-   [YafPluginAbstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.html) - Хук перед відправкою циклу
-   [YafPluginAbstract::preDispatch()](yaf-plugin-abstract.predispatch.html) - Призначення preDispatch
-   [YafPluginAbstract::postDispatch()](yaf-plugin-abstract.postdispatch.html) - Призначення postDispatch
-   [YafPluginAbstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.html) - Призначення dispatchLoopShutdown