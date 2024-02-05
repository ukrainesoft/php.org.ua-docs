---
navigation:
  - yaf-plugin-abstract.preresponse.md: '« Yaf\_Plugin\_Abstract::preResponse'
  - yaf-plugin-abstract.routerstartup.md: 'Yaf\_Plugin\_Abstract::routerStartup »'
  - index.md: PHP Manual
  - class.yaf-plugin-abstract.md: Yaf\_Plugin\_Abstract
title: 'Yaf\_Plugin\_Abstract::routerShutdown'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Plugin\_Abstract::routerShutdown

(Yaf >=1.0.0)

Yaf\_Plugin\_Abstract::routerShutdown — Призначення routerShutdown

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

**Пример #1 Пример использования**Yaf\_Plugin\_Abstract::routerShutdown()\*\*\*\*

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

-   [Yaf\_Plugin\_Abstract::routerStartup()](yaf-plugin-abstract.routerstartup.md) \- Перехоплювач RouterStartup
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.md) \- Хук перед відправкою циклу
-   [Yaf\_Plugin\_Abstract::preDispatch()](yaf-plugin-abstract.predispatch.md) \- Призначення preDispatch
-   [Yaf\_Plugin\_Abstract::postDispatch()](yaf-plugin-abstract.postdispatch.md) \- Призначення postDispatch
-   [Yaf\_Plugin\_Abstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.md) \- Призначення dispatchLoopShutdown
