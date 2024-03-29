---
navigation:
  - ref.win32service.md: « win32service
  - function.win32-create-service.md: win32\_create\_service »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_continue\_service
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_continue\_service

(PECL win32service >=0.1.0)

win32\_continue\_service — Відновлює роботу зупиненої служби

### Опис

```methodsynopsis
win32_continue_service(string $servicename, string $machine = ?): void
```

Відновлює роботу зазначеної зупиненої служби. Вимагає адміністративних привілеїв, або облікового запису з відповідним чином налаштованим ACL для сервісу.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується на локальній машині.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код помилки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

Викидає [ValueError](class.valueerror.md), если значение параметра`servicename`не задано.

Викидає [Win32ServiceException](class.win32serviceexception.md)в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при некоректних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип значення, що повертається void, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |
| PECL win32service 0.3.0 | Ця функція більше не потребує привілею адміністратора, якщо для користувача, що використовується, коректно налаштовано ACL. |

### Дивіться також

-   [win32\_start\_service()](function.win32-start-service.md) \- Запускає службу
-   [win32\_stop\_service()](function.win32-stop-service.md) \- зупиняє службу
-   [win32\_pause\_service()](function.win32-pause-service.md) \- зупиняє службу
-   [win32\_send\_custom\_control()](function.win32-send-custom-control.md) \- Відправляє налаштований елемент керування до служби
-   [Коди Помилок Win32](win32service.constants.errors.md)
