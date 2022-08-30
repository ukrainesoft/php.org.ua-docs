Перехоплювач RouterStartup

-   [« YafPluginAbstract::routerShutdown](yaf-plugin-abstract.routershutdown.html)
    
-   [YafRegistry »](class.yaf-registry.html)
    
-   [PHP Manual](index.html)
    
-   [YafPluginAbstract](class.yaf-plugin-abstract.html)
    
-   Перехоплювач RouterStartup
    

# YafPluginAbstract::routerStartup

(Yaf >=1.0.0)

YafPluginAbstract::routerStartup — Перехоплювач RouterStartup

### Опис

```methodsynopsis
public Yaf_Plugin_Abstract::routerStartup(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
```

Це найраніший перехоплювач у системі плагінів Yaf, якщо плагін реалізує цей метод, то він буде викликаний перед маршрутизацією запиту.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`request`

`response`

### Значення, що повертаються

### Дивіться також

-   [YafPluginAbstract::routerShutdown()](yaf-plugin-abstract.routershutdown.html) - Призначення routerShutdown
-   [YafPluginAbstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.html) - Хук перед відправкою циклу
-   [YafPluginAbstract::preDispatch()](yaf-plugin-abstract.predispatch.html) - Призначення preDispatch
-   [YafPluginAbstract::postDispatch()](yaf-plugin-abstract.postdispatch.html) - Призначення postDispatch
-   [YafPluginAbstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.html) - Призначення dispatchLoopShutdown