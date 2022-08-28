Призначення dispatchLoopShutdown

-   [« Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.html)
    
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup »](yaf-plugin-abstract.dispatchloopstartup.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.html)
    
-   Призначення dispatchLoopShutdown
    

# YafPluginAbstract::dispatchLoopShutdown

(Yaf >=1.0.0)

YafPluginAbstract::dispatchLoopShutdown — Призначення dispatchLoopShutdown

### Опис

```methodsynopsis
public Yaf_Plugin_Abstract::dispatchLoopShutdown(Yaf_Request_Abstract $request, Yaf_Response_Abstract $response): void
```

Це останній перехоплювач у системі підключень плагінів Yaf, якщо плагін реалізує цей метод, то він буде викликаний після завершення циклу диспетчеризації.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`request`

`response`

### Значення, що повертаються

### Дивіться також

-   [Yaf\_Plugin\_Abstract::routerStartup()](yaf-plugin-abstract.routerstartup.html) - Перехоплювач RouterStartup
-   [Yaf\_Plugin\_Abstract::routerShutdown()](yaf-plugin-abstract.routershutdown.html) - Призначення routerShutdown
-   [Yaf\_Plugin\_Abstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.html) - Хук перед відправкою циклу
-   [Yaf\_Plugin\_Abstract::preDispatch()](yaf-plugin-abstract.predispatch.html) - Призначення preDispatch
-   [Yaf\_Plugin\_Abstract::postDispatch()](yaf-plugin-abstract.postdispatch.html) - Призначення postDispatch