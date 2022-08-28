Відправляє налаштований елемент керування до служби

-   [« win32\_query\_service\_status](function.win32-query-service-status.html)
    
-   [win32\_set\_service\_exit\_code »](function.win32-set-service-exit-code.html)
    
-   [PHP Manual](index.html)
    
-   [win32service](ref.win32service.html)
    
-   Відправляє налаштований елемент керування до служби
    

# win32sendcustomcontrol

(PECL win32service >=0.4.0)

win32sendcustomcontrol — Надсилає елемент керування, що настроюється, до служби

### Опис

```methodsynopsis
win32_send_custom_control(string $servicename, int $control, string $machine = ?): void
```

Дивіться [» функцию Microsoft ControlService](https://docs.microsoft.com/en-us/windows/desktop/api/winsvc/nf-winsvc-controlservice) для отримання додаткових відомостей.

### Список параметрів

`servicename`

Коротка назва служби.

`control`

Значення настроюваного елемента управління від 128 до 255.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується локальний комп'ютер.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.html) при невдалому завершенні роботи.

### Помилки

До версії 1.0.0, якщо значення control не знаходиться між 128 та 255, функція видавала помилку рівня **`E_ERROR`**

Викидає [ValueError](class.valueerror.html), якщо значення `servicename` не вказано.

Викидає [ValueError](class.valueerror.html), якщо значення `control` не знаходиться між 128 та 255.

Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки.

### список змін

| Версия                  | Описание                                                                                                                                                              |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.html) при невірних даних у параметрах, що раніше поверталося **`false`**                                                        |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.html) |
| PECL win32service 1.0.0 | Тип повертається тепер void, раніше був [mixed](language.types.declarations.html#language.types.declarations.mixed)                                                   |

### Дивіться також

-   [win32\_start\_service()](function.win32-start-service.html) - Запускає службу
-   [win32\_stop\_service()](function.win32-stop-service.html) - зупиняє службу
-   [win32\_pause\_service()](function.win32-pause-service.html) - зупиняє службу
-   [win32\_continue\_service()](function.win32-continue-service.html) - Відновлює роботу зупиненої служби
-   [Коды ошибок Win32](win32service.constants.errors.html)