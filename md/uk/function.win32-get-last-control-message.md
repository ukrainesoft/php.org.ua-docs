Повертає останнє керуюче повідомлення, яке було надіслано цій службі

-   [« win32\_delete\_service](function.win32-delete-service.html)
    
-   [win32\_pause\_service »](function.win32-pause-service.html)
    
-   [PHP Manual](index.html)
    
-   [win32service](ref.win32service.html)
    
-   Повертає останнє керуюче повідомлення, яке було надіслано цій службі
    

# win32getlastcontrolmessage

(PECL win32service >=0.1.0)

win32getlastcontrolmessage — Повертає останнє повідомлення, яке було надіслано цій службі.

### Опис

```methodsynopsis
win32_get_last_control_message(): int
```

Повертає код, що управляє, останній раз відправлений цьому процесу служби. Під час роботи як служба ви повинні періодично перевіряти це, щоб визначати, чи потрібно вашій службі припинити роботу.

**Застереження**

Починаючи з версії 0.2.0, функція працює лише у "cli" SAPI. На інших SAPI цю функцію вимкнено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає керуючу константу, яка буде однією з [Констант сообщений управления службой Win32Service](win32service.constants.servicecontrol.html) **`WIN32_SERVICE_CONTROL_CONTINUE`** **`WIN32_SERVICE_CONTROL_DEVICEEVENT`** **`WIN32_SERVICE_CONTROL_HARDWAREPROFILECHANGE`** **`WIN32_SERVICE_CONTROL_INTERROGATE`** **`WIN32_SERVICE_CONTROL_NETBINDADD`** **`WIN32_SERVICE_CONTROL_NETBINDDISABLE`** **`WIN32_SERVICE_CONTROL_NETBINDENABLE`** **`WIN32_SERVICE_CONTROL_NETBINDREMOVE`** **`WIN32_SERVICE_CONTROL_PARAMCHANGE`** **`WIN32_SERVICE_CONTROL_PAUSE`** **`WIN32_SERVICE_CONTROL_POWEREVENT`** **`WIN32_SERVICE_CONTROL_PRESHUTDOWN`** **`WIN32_SERVICE_CONTROL_SESSIONCHANGE`** **`WIN32_SERVICE_CONTROL_SHUTDOWN`** **`WIN32_SERVICE_CONTROL_STOP`**

Якщо значення знаходиться в діапазоні від 128 до 255, код керування налаштовується.

### Помилки

До версії 1.0.0, якщо SAPI не `"cli"`, функція видавала помилку рівня **`E_ERROR`**

Починаючи з версії 1.0.0, викидає [Win32ServiceException](class.win32serviceexception.html), якщо SAPI не `"cli"`

### список змін

| Версия                  | Описание                                                                                                                                                              |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.html) при невірних даних у параметрах, що раніше поверталося **`false`**                                                        |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.html) |
| PECL win32service 0.2.0 | Функція працює тільки з `"cli"` SAPI.                                                                                                                                 |

### Дивіться також

-   [win32\_start\_service\_ctrl\_dispatcher()](function.win32-start-service-ctrl-dispatcher.html) - Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям
-   [win32\_set\_service\_status()](function.win32-set-service-status.html) - Оновлює статус служби
-   [win32\_set\_service\_exit\_mode()](function.win32-set-service-exit-mode.html) - Визначає або повертає режим виходу для поточної запущеної служби
-   [win32\_set\_service\_exit\_code()](function.win32-set-service-exit-code.html) - Визначає чи повертає код виходу для поточної запущеної служби
-   [Константы сообщений управления службой Win32Service](win32service.constants.servicecontrol.html)