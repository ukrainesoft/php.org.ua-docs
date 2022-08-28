Припиняє службу

-   [« win32\_get\_last\_control\_message](function.win32-get-last-control-message.html)
    
-   [win32\_query\_service\_status »](function.win32-query-service-status.html)
    
-   [PHP Manual](index.html)
    
-   [win32service](ref.win32service.html)
    
-   Припиняє службу
    

# win32pauseservice

(PECL win32service >=0.1.0)

win32pauseservice — Зупиняє службу

### Опис

```methodsynopsis
win32_pause_service(string $servicename, string $machine = ?): void
```

Зупиняє вказану службу. Потрібні адміністративні привілеї або обліковий запис з відповідними правами, встановленими в службі ACL.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується локальний комп'ютер.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.html) при невдалому завершенні роботи.

### Помилки

Викидає [ValueError](class.valueerror.html), якщо значення `servicename` не вказано.

Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.html) при невірних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.html) |
| PECL win32service 1.0.0 | Тип повертається тепер void, раніше був [mixed](language.types.declarations.html#language.types.declarations.mixed) |
| PECL win32service 0.3.0 | Функція більше не вимагає облікового запису адміністратора, якщо ACL інстальовано для іншого облікового запису. |

### Дивіться також

-   [win32\_start\_service()](function.win32-start-service.html) - Запускає службу
-   [win32\_stop\_service()](function.win32-stop-service.html) - зупиняє службу
-   [win32\_continue\_service()](function.win32-continue-service.html) - Відновлює роботу зупиненої служби
-   [win32\_send\_custom\_control()](function.win32-send-custom-control.html) - Відправляє налаштований елемент керування до служби
-   [Коды ошибок Win32](win32service.constants.errors.html)