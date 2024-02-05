---
navigation:
  - function.win32-query-service-status.md: « win32\_query\_service\_status
  - function.win32-set-service-exit-code.md: win32\_set\_service\_exit\_code »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_send\_custom\_control
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_send\_custom\_control

(PECL win32service >=0.4.0)

win32\_send\_custom\_control — Надсилає елемент керування, що настроюється, до служби

### Опис

```methodsynopsis
win32_send_custom_control(string $servicename, int $control, string $machine = ?): void
```

Смотрите[» функцію Microsoft ControlService](https://docs.microsoft.com/en-us/windows/desktop/api/winsvc/nf-winsvc-controlservice) для отримання додаткових відомостей.

### Список параметрів

`servicename`

Коротка назва служби.

`control`

Значення настроюваного елемента керування від 128 до 255.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується локальний комп'ютер.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код помилки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

До версії 1.0.0, якщо значення control не знаходиться між 128 та 255, функція видавала помилку рівня **`E_ERROR`**

Викидає [ValueError](class.valueerror.md), если значение`servicename` не вказано.

Викидає [ValueError](class.valueerror.md), если значение`control` не знаходиться між 128 та 255.

Викидає [Win32ServiceException](class.win32serviceexception.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип повертається тепер void, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |

### Дивіться також

-   [win32\_start\_service()](function.win32-start-service.md) \- Запускає службу
-   [win32\_stop\_service()](function.win32-stop-service.md) \- зупиняє службу
-   [win32\_pause\_service()](function.win32-pause-service.md) \- зупиняє службу
-   [win32\_continue\_service()](function.win32-continue-service.md) \- Відновлює роботу зупиненої служби
-   [Коди помилок Win32](win32service.constants.errors.md)
