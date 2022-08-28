Встановити функцію зворотного виклику, коли завдання ставиться у чергу

-   [« GearmanClient::setContext](gearmanclient.setcontext.html)
    
-   [GearmanClient::setData »](gearmanclient.setdata.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Встановити функцію зворотного виклику, коли завдання ставиться у чергу
    

# GearmanClient::setCreatedCallback

(PECL gearman >= 0.5.0)

GearmanClient::setCreatedCallback — Встановити функцію зворотного дзвінка, коли завдання ставиться в чергу

### Опис

```methodsynopsis
public GearmanClient::setCreatedCallback(string $callback): bool
```

Встановлює функцію, яка буде викликана, коли завдання отримано та поставлено в чергу сервером задач Gearman. Функція зворотного виклику повинна приймати єдиний параметр – об'єкт [GearmanTask](class.gearmantask.html)

### Список параметрів

`callback`

Функція, яка має бути викликана.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань
-   [GearmanClient::setWorkloadCallback()](gearmanclient.setworkloadcallback.html) - Установка callback-функції, яка приймає проміжні результати від оброблювача завдань