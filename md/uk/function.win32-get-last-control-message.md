---
navigation:
  - function.win32-delete-service.md: « win32\_delete\_service
  - function.win32-pause-service.md: win32\_pause\_service »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_get\_last\_control\_message
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_get\_last\_control\_message

(PECL win32service >=0.1.0)

win32\_get\_last\_control\_message — Повертає останнє повідомлення, яке було надіслано цій службі.

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

Повертає керуючу константу, яка буде однією з [Констант повідомлень керування службою Win32Service](win32service.constants.servicecontrol.md) **`WIN32_SERVICE_CONTROL_CONTINUE`** **`WIN32_SERVICE_CONTROL_DEVICEEVENT`** **`WIN32_SERVICE_CONTROL_HARDWAREPROFILECHANGE`** **`WIN32_SERVICE_CONTROL_INTERROGATE`** **`WIN32_SERVICE_CONTROL_NETBINDADD`** **`WIN32_SERVICE_CONTROL_NETBINDDISABLE`** **`WIN32_SERVICE_CONTROL_NETBINDENABLE`** **`WIN32_SERVICE_CONTROL_NETBINDREMOVE`** **`WIN32_SERVICE_CONTROL_PARAMCHANGE`** **`WIN32_SERVICE_CONTROL_PAUSE`** **`WIN32_SERVICE_CONTROL_POWEREVENT`** **`WIN32_SERVICE_CONTROL_PRESHUTDOWN`** **`WIN32_SERVICE_CONTROL_SESSIONCHANGE`** **`WIN32_SERVICE_CONTROL_SHUTDOWN`** **`WIN32_SERVICE_CONTROL_STOP`**

Якщо значення знаходиться в діапазоні від 128 до 255, код керування налаштовується.

### Помилки

До версії 1.0.0, якщо SAPI не `"cli"`, функція видавала помилку рівня **`E_ERROR`**

Починаючи з версії 1.0.0, викидає [Win32ServiceException](class.win32serviceexception.md), якщо SAPI не `"cli"`

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 0.2.0 | Функція працює тільки з `"cli"`SAPI. |

### Дивіться також

-   [win32\_start\_service\_ctrl\_dispatcher()](function.win32-start-service-ctrl-dispatcher.md) \- Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям
-   [win32\_set\_service\_status()](function.win32-set-service-status.md) \- Оновлює статус служби
-   [win32\_set\_service\_exit\_mode()](function.win32-set-service-exit-mode.md) \- Визначає або повертає режим виходу для поточної запущеної служби
-   [win32\_set\_service\_exit\_code()](function.win32-set-service-exit-code.md) \- Визначає чи повертає код виходу для поточної запущеної служби
-   [Константи повідомлень керування службою Win32Service](win32service.constants.servicecontrol.md)
