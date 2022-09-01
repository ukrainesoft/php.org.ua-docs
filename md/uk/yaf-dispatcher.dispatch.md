---
navigation:
  - yaf-dispatcher.disableview.html: '« YafDispatcher::disableView'
  - yaf-dispatcher.enableview.html: 'YafDispatcher::enableView »'
  - index.html: PHP Manual
  - class.yaf-dispatcher.html: YafDispatcher
title: 'YafDispatcher::dispatch'
---
# YafDispatcher::dispatch

(Yaf >=1.0.0)

YafDispatcher::dispatch — Надсилає запит

### Опис

```methodsynopsis
public Yaf_Dispatcher::dispatch(Yaf_Request_Abstract $request): Yaf_Response_Abstract
```

Метод виконує важку роботу [YafDispatcher](class.yaf-dispatcher.html). Потрібний об'єкт запиту.

Процес відправлення має три різні події:

-   Маршрутизація
-   Диспетчеризація
-   Відповідь

Маршрутизація виконується рівно один раз з використанням значень в об'єкті запиту під час виклику **YafDispatcher::dispatch()**. Диспетчеризація відбувається у циклі; запит може або вказувати на кілька дій для відправки, або контролер або модуль, що підключається може скинути об'єкт запиту, щоб примусово виконати відправку додаткових дій (дивіться [YafPluginAbstract](class.yaf-plugin-abstract.html). Коли все буде готове, [YafDispatcher](class.yaf-dispatcher.html) повертає відповідь.

### Список параметрів

`request`

### Значення, що повертаються
