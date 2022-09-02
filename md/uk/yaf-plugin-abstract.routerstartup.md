---
navigation:
  - yaf-plugin-abstract.routershutdown.md: '« YafPluginAbstract::routerShutdown'
  - class.yaf-registry.md: YafRegistry »
  - index.md: PHP Manual
  - class.yaf-plugin-abstract.md: YafPluginAbstract
title: 'YafPluginAbstract::routerStartup'
---
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

-   [YafPluginAbstract::routerShutdown()](yaf-plugin-abstract.routershutdown.md) - Призначення routerShutdown
-   [YafPluginAbstract::dispatchLoopStartup()](yaf-plugin-abstract.dispatchloopstartup.md) - Хук перед відправкою циклу
-   [YafPluginAbstract::preDispatch()](yaf-plugin-abstract.predispatch.md) - Призначення preDispatch
-   [YafPluginAbstract::postDispatch()](yaf-plugin-abstract.postdispatch.md) - Призначення postDispatch
-   [YafPluginAbstract::dispatchLoopShutdown()](yaf-plugin-abstract.dispatchloopshutdown.md) - Призначення dispatchLoopShutdown
