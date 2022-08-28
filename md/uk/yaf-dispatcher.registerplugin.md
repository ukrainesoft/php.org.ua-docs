Реєструє плагін

-   [« Yaf\_Dispatcher::initView](yaf-dispatcher.initview.html)
    
-   [Yaf\_Dispatcher::returnResponse »](yaf-dispatcher.returnresponse.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Dispatcher](class.yaf-dispatcher.html)
    
-   Реєструє плагін
    

# YafDispatcher::registerPlugin

(Yaf >=1.0.0)

YafDispatcher::registerPlugin — Реєструє плагін

### Опис

```methodsynopsis
public Yaf_Dispatcher::registerPlugin(Yaf_Plugin_Abstract $plugin): Yaf_Dispatcher
```

Реєструє плагін (дивіться [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.html)). Як правило, ми реєструємо плагіни в Bootstrap (дивіться [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.html)

### Список параметрів

`plugin`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **YafDispatcher::registerPlugin()****

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract {
  public function _initPlugin(Yaf_Dispatcher $dispatcher) {
    /**
    * Yaf ожидает скрипты плагинов в [application.directory] .  "/plugins"
    * для этого случая будет:
    * [application.directory] . "/plugins/" . "User" . [application.ext]
    */
    $user = new UserPlugin();
    $dispatcher->registerPlugin($user);
  }
}
?>
```

### Дивіться також

-   [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.html)
    
-   [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.html)