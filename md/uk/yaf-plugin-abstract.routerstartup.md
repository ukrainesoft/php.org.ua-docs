Перехоплювач RouterStartup

-   [« Yaf\_Plugin\_Abstract::routerShutdown](yaf-plugin-abstract.routershutdown.html)
    
-   [Yaf\_Registry »](class.yaf-registry.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.html)
    
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

-   [Yaf\_Plugin\_Abstract::routerShutdown()](yaf-plugin-abstract.routershutdown.html) - Призначення routerShutdown
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.html) - Хук перед відправкою циклу
-   [Yaf\_Plugin\_Abstract::preDispatch()](yaf-plugin-abstract.predispatch.html) - Призначення preDispatch
-   [Yaf\_Plugin\_Abstract::postDispatch()](yaf-plugin-abstract.postdispatch.html) - Призначення postDispatch
-   [Yaf\_Plugin\_Abstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.html) - Призначення dispatchLoopShutdown