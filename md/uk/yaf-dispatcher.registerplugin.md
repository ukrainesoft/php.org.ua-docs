---
navigation:
  - yaf-dispatcher.initview.html: '« YafDispatcher::initView'
  - yaf-dispatcher.returnresponse.html: 'YafDispatcher::returnResponse »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.html: YafDispatcher
title: 'YafDispatcher::registerPlugin'
---
# YafDispatcher::registerPlugin

(Yaf >=1.0.0)

YafDispatcher::registerPlugin — Реєструє плагін

### Опис

```methodsynopsis
public Yaf_Dispatcher::registerPlugin(Yaf_Plugin_Abstract $plugin): Yaf_Dispatcher
```

Реєструє плагін (дивіться [YafPluginAbstract](class.yaf-plugin-abstract.html)). Як правило, ми реєструємо плагіни в Bootstrap (дивіться [YafBootstrapAbstract](class.yaf-bootstrap-abstract.html)

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

-   [YafPluginAbstract](class.yaf-plugin-abstract.html)
    
-   [YafBootstrapAbstract](class.yaf-bootstrap-abstract.html)
