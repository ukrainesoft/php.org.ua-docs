---
navigation:
  - class.yaf-plugin-abstract.html: « YafPluginAbstract
  - yaf-plugin-abstract.dispatchloopstartup.html: 'YafPluginAbstract::dispatchLoopStartup »'
  - index.md: PHP Manual
  - class.yaf-plugin-abstract.html: YafPluginAbstract
title: 'YafPluginAbstract::dispatchLoopShutdown'
---
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

-   [YafPluginAbstract::routerStartup()](yaf-plugin-abstract.routerstartup.md) - Перехоплювач RouterStartup
-   [YafPluginAbstract::routerShutdown()](yaf-plugin-abstract.routershutdown.md) - Призначення routerShutdown
-   [YafPluginAbstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.md) - Хук перед відправкою циклу
-   [YafPluginAbstract::preDispatch()](yaf-plugin-abstract.predispatch.md) - Призначення preDispatch
-   [YafPluginAbstract::postDispatch()](yaf-plugin-abstract.postdispatch.md) - Призначення postDispatch
