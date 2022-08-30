Запускає службу

-   [« win32startservicectrldispatcher](function.win32-start-service-ctrl-dispatcher.html)
    
-   [win32stopservice »](function.win32-stop-service.html)
    
-   [PHP Manual](index.md)
    
-   [win32service](ref.win32service.md)
    
-   Запускає службу
    

# win32startservice

(PECL win32service >=0.1.0)

win32startservice — Запуск служби

### Опис

```methodsynopsis
win32_start_service(string $servicename, string $machine = ?): void
```

Здійснює спробу запуску зазначеної служби. Зазвичай вимагає адміністративних привілеїв або облікового запису з відповідним чином налаштованим ACL для сервісу.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується на локальній машині.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

Викидає [ValueError](class.valueerror.md), якщо значення параметра `servicename` не задано.

Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки.

### список змін

| Версия                  | Описание                                                                                                                                                          |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при некоректних даних у параметрах, що раніше поверталося **`false`**                                                   |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип значення, що повертається void, раніше був [mixed](language.types.declarations.html#language.types.declarations.mixed)                                        |
| PECL win32service 0.3.0 | Ця функція більше не потребує привілею адміністратора, якщо коректно налаштовано ACL для користувача, що використовується.                                        |

### Дивіться також

-   [win32stopservice()](function.win32-stop-service.html) - зупиняє службу
-   [win32pauseservice()](function.win32-pause-service.html) - зупиняє службу
-   [win32continueservice()](function.win32-continue-service.html) - Відновлює роботу зупиненої служби
-   [win32sendcustomcontrol()](function.win32-send-custom-control.html) - Відправляє налаштований елемент керування до служби
-   [Коди Помилок Win32](win32service.constants.errors.md)