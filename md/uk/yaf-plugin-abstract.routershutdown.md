---
navigation:
  - yaf-plugin-abstract.preresponse.md: '« YafPluginAbstract::preResponse'
  - yaf-plugin-abstract.routerstartup.md: 'YafPluginAbstract::routerStartup »'
  - index.md: PHP Manual
  - class.yaf-plugin-abstract.md: YafPluginAbstract
title: 'YafPluginAbstract::routerShutdown'
---
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
class UserInitPlugin extends Yaf_Plugin_Abstract {

    public function routerShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response) {
        $controller = $request->getControllerName();

        /**
         * Использовать контроллер доступа не нужно для API
         */
        if (in_array(strtolower($controller), array(
            'api',
        ))) {
            return TRUE;
        }

        if (Yaf_Session::getInstance()->has("login")) {
            return TRUE;
        }

        /* Ошибка проверки доступа, необходимо войти */
        $response->setRedirect("http://yourdomain.com/login/");
        return FALSE;
    }
}
?>
```

### Дивіться також

-   [YafPluginAbstract::routerStartup()](yaf-plugin-abstract.routerstartup.md) - Перехоплювач RouterStartup
-   [YafPluginAbstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.md) - Хук перед відправкою циклу
-   [YafPluginAbstract::preDispatch()](yaf-plugin-abstract.predispatch.md) - Призначення preDispatch
-   [YafPluginAbstract::postDispatch()](yaf-plugin-abstract.postdispatch.md) - Призначення postDispatch
-   [YafPluginAbstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.md) - Призначення dispatchLoopShutdown
