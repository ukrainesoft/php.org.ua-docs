Зупиняє службу

-   [« win32startservice](function.win32-start-service.html)
    
-   [Обработка XML »](refs.xml.html)
    
-   [PHP Manual](index.html)
    
-   [win32service](ref.win32service.html)
    
-   Зупиняє службу
    

# win32stopservice

(PECL win32service >=0.1.0)

win32stopservice - Зупиняє службу

### Опис

```methodsynopsis
win32_stop_service(string $servicename, string $machine = ?): void
```

Зупиняє зазначену службу. Вимагає адміністративних привілеїв, або облікового запису з відповідним чином налаштованим ACL для сервісу.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовується на локальній машині.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.html) при невдалому завершенні роботи.

### Помилки

Викидає [ValueError](class.valueerror.html), якщо значення параметра `servicename` не задано.

Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки.

### список змін

| Версия                  | Описание                                                                                                                                                              |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.html) при некоректних даних у параметрах, що раніше поверталося **`false`**                                                     |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.html) |
| PECL win32service 1.0.0 | Тип значення, що повертається void, раніше був [mixed](language.types.declarations.html#language.types.declarations.mixed)                                            |
| PECL win32service 0.3.0 | Ця функція більше не потребує привілею адміністратора, якщо коректно налаштовано ACL для користувача, що використовується.                                            |

### Дивіться також

-   [win32startservice()](function.win32-start-service.html) - Запускає службу
-   [win32pauseservice()](function.win32-pause-service.html) - зупиняє службу
-   [win32continueservice()](function.win32-continue-service.html) - Відновлює роботу зупиненої служби
-   [win32sendcustomcontrol()](function.win32-send-custom-control.html) - Відправляє налаштований елемент керування до служби
-   [Коди Помилок Win32](win32service.constants.errors.html)