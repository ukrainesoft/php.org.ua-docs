Установка callback-функції, яка приймає проміжні результати від оброблювача завдань

-   [« GearmanClient::setWarningCallback](gearmanclient.setwarningcallback.html)
    
-   [GearmanClient::timeout »](gearmanclient.timeout.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Установка callback-функції, яка приймає проміжні результати від оброблювача завдань
    

# GearmanClient::setWorkloadCallback

(PECL gearman >= 0.5.0)

GearmanClient::setWorkloadCallback — Встановлення callback-функції, яка приймає проміжні результати від обробника завдань

### Опис

```methodsynopsis
public GearmanClient::setWorkloadCallback(callable $callback): bool
```

Задає функцію, яка буде викликатись, коли обробнику завдання необхідно передати проміжні результати клієнту до завершення всієї обробки. Обробнику завдань може знадобитися таке пересилання, якщо потрібно передати клієнту будь-які оновлення, частково надіслати результати обробки або звільнити пам'ять під час виконання довгих завдань. Функція має приймати один аргумент типу [GearmanTask](class.gearmantask.html)

### Список параметрів

`callback`

Функція зворотного дзвінка

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanClient::setDataCallback()](gearmanclient.setdatacallback.html) - Задає callback-функцію обробки переданих даних
-   [GearmanClient::setCompleteCallback()](gearmanclient.setcompletecallback.html) - Встановіть функцію, яка буде викликана після завершення завдання
-   [GearmanClient::setCreatedCallback()](gearmanclient.setcreatedcallback.html) - Встановити функцію зворотного виклику, коли завдання ставиться у чергу
-   [GearmanClient::setExceptionCallback()](gearmanclient.setexceptioncallback.html) - Встановлення функції зворотного дзвінка для перехоплення виключень обробника завдань
-   [GearmanClient::setFailCallback()](gearmanclient.setfailcallback.html) - Установка callback-функції для обробки ситуації, коли завдання не вдалося виконати
-   [GearmanClient::setStatusCallback()](gearmanclient.setstatuscallback.html) - завдання callback-функції, що збирає інформацію про стан обробника завдань
-   [GearmanClient::setWarningCallback()](gearmanclient.setwarningcallback.html) - Установка callback-функції, яка обслуговує попередження оброблювача завдань