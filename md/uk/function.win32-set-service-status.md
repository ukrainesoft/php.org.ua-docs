Оновлює статус служби

-   [« win32setserviceexitmode](function.win32-set-service-exit-mode.html)
    
-   [win32startservicectrldispatcher »](function.win32-start-service-ctrl-dispatcher.html)
    
-   [PHP Manual](index.md)
    
-   [win32service](ref.win32service.md)
    
-   Оновлює статус служби
    

# win32setservicestatus

(PECL win32service >=0.1.0)

win32setservicestatus — Оновлює статус служби

### Опис

```methodsynopsis
win32_set_service_status(int $status, int $checkpoint = 0): void
```

Повідомляє SCM про поточний стан працюючої служби. Цей дзвінок дійсний лише для запущеного сервісного процесу.

**Застереження**

Починаючи з версії 0.2.0, функція працює лише у "cli" SAPI. На інших SAPI цю функцію вимкнено.

### Список параметрів

`status`

Код статусу служби, один із: **`WIN32_SERVICE_RUNNING`** **`WIN32_SERVICE_STOPPED`** **`WIN32_SERVICE_STOP_PENDING`** **`WIN32_SERVICE_START_PENDING`** **`WIN32_SERVICE_CONTINUE_PENDING`** **`WIN32_SERVICE_PAUSE_PENDING`** **`WIN32_SERVICE_PAUSED`**

`checkpoint`

Значення контрольної точки, яке періодично збільшує служба, щоб повідомити про свій прогрес під час тривалого запуску, зупинки, паузи або продовження роботи. Наприклад, служба повинна збільшувати це значення на одиницю в міру завершення кожного кроку своєї ініціалізації під час запуску.

`checkpoint` дійсна лише тоді, коли `status` є одним з **`WIN32_SERVICE_STOP_PENDING`** **`WIN32_SERVICE_START_PENDING`** **`WIN32_SERVICE_CONTINUE_PENDING`** або **`WIN32_SERVICE_PAUSE_PENDING`**

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

До версії 1.0.0, якщо SAPI не `"cli"`, функція видавала помилку рівня **`E_ERROR`**

Починаючи з версії 1.0.0, викидає [Win32ServiceException](class.win32serviceexception.md), якщо SAPI не `"cli"`

### список змін

| Версия | Описание |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип повертається тепер void, раніше був [mixed](language.types.declarations.html#language.types.declarations.mixed) |
| PECL win32service 0.2.0 | Функція працює тільки з `"cli"` SAPI. |

### Дивіться також

-   [win32startservicectrldispatcher()](function.win32-start-service-ctrl-dispatcher.html) - Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям
-   [win32getlastcontrolmessage()](function.win32-get-last-control-message.html) - Повертає останнє керуюче повідомлення, яке було надіслано цій службі
-   [win32setserviceexitmode()](function.win32-set-service-exit-mode.html) - Визначає або повертає режим виходу для поточної запущеної служби
-   [win32setserviceexitcode()](function.win32-set-service-exit-code.html) - Визначає чи повертає код виходу для поточної запущеної служби
-   [Константи стану служби Win32Service](win32service.constants.servicestatus.md)