---
navigation:
  - function.win32-set-service-exit-code.html: « win32setserviceexitcode
  - function.win32-set-service-status.html: win32setservicestatus »
  - index.html: PHP Manual
  - ref.win32service.html: win32service
title: win32setserviceexitmode
---
# win32setserviceexitmode

(PECL win32service >=0.4.0)

win32setserviceexitmode — Визначає або повертає вихідний режим для поточної запущеної служби

### Опис

```methodsynopsis
win32_set_service_exit_mode(bool $gracefulMode = true): bool
```

Якщо вказано параметр `gracefulMode`, режим виходу змінюється. Коли режим виходу не є коректним, код виходу, що використовується, може бути встановлений за допомогою функції [win32setserviceexitcode()](function.win32-set-service-exit-code.html)

**Застереження**

Функція працює лише у "cli" SAPI. На інших SAPI цю функцію вимкнено.

### Список параметрів

`gracefulMode`

**`true`** для витонченого виходу . **`false`** для виходу із помилкою.

### Значення, що повертаються

Повертає поточний або старий режим виходу.

### Помилки

До версії 1.0.0, якщо SAPI не `"cli"`, функція видавала помилку рівня **`E_ERROR`**

Починаючи з версії 1.0.0, викидає [Win32ServiceException](class.win32serviceexception.html), якщо SAPI не `"cli"`

### список змін

| Версия | Описание |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.html) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.html) |

### Дивіться також

-   [win32startservicectrldispatcher()](function.win32-start-service-ctrl-dispatcher.html) - Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям
-   [win32setservicestatus()](function.win32-set-service-status.html) - Оновлює статус служби
-   [win32setserviceexitcode()](function.win32-set-service-exit-code.html) - Визначає чи повертає код виходу для поточної запущеної служби
