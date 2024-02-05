---
navigation:
  - yaf-dispatcher.initview.md: '« Yaf\_Dispatcher::initView'
  - yaf-dispatcher.returnresponse.md: 'Yaf\_Dispatcher::returnResponse »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: Yaf\_Dispatcher
title: 'Yaf\_Dispatcher::registerPlugin'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Dispatcher::registerPlugin

(Yaf >=1.0.0)

Yaf\_Dispatcher::registerPlugin — Реєструє плагін

### Опис

```methodsynopsis
public Yaf_Dispatcher::registerPlugin(Yaf_Plugin_Abstract $plugin): Yaf_Dispatcher
```

Регистрирует плагин (смотрите[Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.md)). Як правило, ми реєструємо плагіни в Bootstrap (дивіться [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.md)

### Список параметрів

`plugin`

### Значення, що повертаються

### Приклади

**Пример #1 Пример использования**Yaf\_Dispatcher::registerPlugin()\*\*\*\*

```php
<?php
class Bootstrap extends Yaf_Bootstrap_Abstract {
  public function _initPlugin(Yaf_Dispatcher $dispatcher) {
    /**
    * Yaf ожидает скрипты плагинов в [application.directory] .  "/plugins"
    * для этого случая будет:
    * [application.directory] . "/plugins/" . "User" . [application.ext]
    */
    $user = new UserPlugin();
    $dispatcher->registerPlugin($user);
  }
}
?>
```

### Дивіться також

-   [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.md)
    
-   [Yaf\_Bootstrap\_Abstract](class.yaf-bootstrap-abstract.md)
