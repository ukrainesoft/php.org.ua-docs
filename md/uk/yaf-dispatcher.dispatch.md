---
navigation:
  - yaf-dispatcher.disableview.md: '« Yaf\_Dispatcher::disableView'
  - yaf-dispatcher.enableview.md: 'Yaf\_Dispatcher::enableView »'
  - index.md: PHP Manual
  - class.yaf-dispatcher.md: Yaf\_Dispatcher
title: 'Yaf\_Dispatcher::dispatch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yaf\_Dispatcher::dispatch

(Yaf >=1.0.0)

Yaf\_Dispatcher::dispatch — Надсилає запит

### Опис

```methodsynopsis
public Yaf_Dispatcher::dispatch(Yaf_Request_Abstract $request): Yaf_Response_Abstract
```

Метод виконує важку роботу [Yaf\_Dispatcher](class.yaf-dispatcher.md). Потрібний об'єкт запиту.

Процес відправлення має три різні події:

-   Маршрутизація
-   Диспетчеризація
-   Відповідь

Маршрутизація виконується рівно один раз з використанням значень в об'єкті запиту під час виклику **Yaf\_Dispatcher::dispatch()**. Диспетчеризація відбувається у циклі; запит може або вказувати на кілька дій для відправки, або контролер або модуль, що підключається може скинути об'єкт запиту, щоб примусово виконати відправку додаткових дій (дивіться [Yaf\_Plugin\_Abstract](class.yaf-plugin-abstract.md). Коли все буде готове, [Yaf\_Dispatcher](class.yaf-dispatcher.md) повертає відповідь.

### Список параметрів

`request`

### Значення, що повертаються
