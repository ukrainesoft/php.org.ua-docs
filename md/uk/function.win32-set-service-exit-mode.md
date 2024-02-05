---
navigation:
  - function.win32-set-service-exit-code.md: « win32\_set\_service\_exit\_code
  - function.win32-set-service-status.md: win32\_set\_service\_status »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_set\_service\_exit\_mode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_set\_service\_exit\_mode

(PECL win32service >=0.4.0)

win32\_set\_service\_exit\_mode — Визначає або повертає вихідний режим для поточної запущеної служби

### Опис

```methodsynopsis
win32_set_service_exit_mode(bool $gracefulMode = true): bool
```

Если указан параметр`gracefulMode`, режим виходу змінюється. Коли режим виходу не є коректним, код виходу, що використовується, може бути встановлений за допомогою функції [win32\_set\_service\_exit\_code()](function.win32-set-service-exit-code.md)

**Застереження**

Функція працює лише у "cli" SAPI. На інших SAPI цю функцію вимкнено.

### Список параметрів

`gracefulMode`

**`true`** для витонченого виходу . **`false`** для виходу із помилкою.

### Значення, що повертаються

Повертає поточний або старий режим виходу.

### Помилки

До версії 1.0.0, якщо SAPI не `"cli"`, функція видавала помилку рівня **`E_ERROR`**

Починаючи з версії 1.0.0, викидає [Win32ServiceException](class.win32serviceexception.md), якщо SAPI не `"cli"`

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |

### Дивіться також

-   [win32\_start\_service\_ctrl\_dispatcher()](function.win32-start-service-ctrl-dispatcher.md) \- Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям
-   [win32\_set\_service\_status()](function.win32-set-service-status.md) \- Оновлює статус служби
-   [win32\_set\_service\_exit\_code()](function.win32-set-service-exit-code.md) \- Визначає чи повертає код виходу для поточної запущеної служби
