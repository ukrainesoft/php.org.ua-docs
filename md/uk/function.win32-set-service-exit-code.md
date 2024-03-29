---
navigation:
  - function.win32-send-custom-control.md: « win32\_send\_custom\_control
  - function.win32-set-service-exit-mode.md: win32\_set\_service\_exit\_mode »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_set\_service\_exit\_code
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_set\_service\_exit\_code

(PECL win32service >=0.4.0)

win32\_set\_service\_exit\_code — Визначає або повертає вихідний код для поточної запущеної служби

### Опис

```methodsynopsis
win32_set_service_exit_code(int $exitCode = 1): int
```

Змінює чи повертає код виходу. Код виходу використовується лише в тому випадку, якщо режим виходу не витончений. Якщо значення не дорівнює нулю, конфігурацію відновлення можна використовувати після збою обслуговування. Дивіться [» коди системних помилок Microsoft](https://docs.microsoft.com/en-us/windows/desktop/debug/system-error-codes) для отримання додаткових відомостей.

**Застереження**

Функція працює лише у "cli" SAPI. На інших SAPI цю функцію вимкнено.

### Список параметрів

`exitCode`

Код повернення, який використовується при виході.

### Значення, що повертаються

Повертає поточний або старий вихідний код.

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
-   [win32\_set\_service\_exit\_mode()](function.win32-set-service-exit-mode.md) \- Визначає або повертає режим виходу для поточної запущеної служби
