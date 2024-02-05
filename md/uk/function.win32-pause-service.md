---
navigation:
  - function.win32-get-last-control-message.md: « win32\_get\_last\_control\_message
  - function.win32-query-service-status.md: win32\_query\_service\_status »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_pause\_service
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_pause\_service

(PECL win32service >=0.1.0)

win32\_pause\_service — Зупиняє службу

### Опис

```methodsynopsis
win32_pause_service(string $servicename, string $machine = ?): void
```

Припиняє вказану службу. Потрібні адміністративні привілеї або обліковий запис з відповідними правами, встановленими в службі ACL.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується локальний комп'ютер.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код помилки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

Викидає [ValueError](class.valueerror.md), если значение`servicename` не вказано.

Викидає [Win32ServiceException](class.win32serviceexception.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип повертається тепер void, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |
| PECL win32service 0.3.0 | Функція більше не вимагає облікового запису адміністратора, якщо ACL інстальовано для іншого облікового запису. |

### Дивіться також

-   [win32\_start\_service()](function.win32-start-service.md) \- Запускає службу
-   [win32\_stop\_service()](function.win32-stop-service.md) \- зупиняє службу
-   [win32\_continue\_service()](function.win32-continue-service.md) \- Відновлює роботу зупиненої служби
-   [win32\_send\_custom\_control()](function.win32-send-custom-control.md) \- Відправляє налаштований елемент керування до служби
-   [Коди помилок Win32](win32service.constants.errors.md)
