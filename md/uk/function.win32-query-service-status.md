Запитує статус сервісу

-   [« win32pauseservice](function.win32-pause-service.html)
    
-   [win32sendcustomcontrol »](function.win32-send-custom-control.html)
    
-   [PHP Manual](index.html)
    
-   [win32service](ref.win32service.html)
    
-   Запитує статус сервісу
    

# win32queryservicestatus

(PECL win32service >=0.1.0)

win32queryservicestatus — Запитує статус сервісу

### Опис

```methodsynopsis
win32_query_service_status(string $servicename, string $machine = ?): array
```

Вимагає поточний статус служби, повертаючи масив інформації.

### Список параметрів

`servicename`

Коротка назва служби.

`machine`

Необов'язкове ім'я машини. Якщо не вказано, використовуватиметься локальний комп'ютер.

### Значення, що повертаються

Повертає масив, що складається з наступної інформації у разі успішного виконання:

До версії 1.0.0 **`false`** якщо була виявлена ​​проблема з параметрами або [код ошибки Win32](win32service.constants.errors.html) при невдалому завершенні роботи.

`ServiceType`

dwServiceType. Дивіться [Побутові маски типів служби Win32Service](win32service.constants.servicetype.html)

`CurrentState`

dwCurrentState. Дивіться [Константи стану служби Win32Service](win32service.constants.servicestatus.html)

`ControlsAccepted`

Які елементи керування службами приймаються службою. Дивіться [Битовые маски Win32Service Service Control Message Accepted](win32service.constants.controlsaccepted.html)

`Win32ExitCode`

Якщо служба завершила роботу, тут з'являється код повернення з процесу. Це значення дорівнює \*\*`WIN32_ERROR_SERVICE_SPECIFIC_ERROR`\*\*якщо режим виходу не є плавним. Дивіться [коды ошибок Win32Service](win32service.constants.errors.html) і [win32setserviceexitmode()](function.win32-set-service-exit-mode.html)

`ServiceSpecificExitCode`

Якщо служба завершила роботу, тут відображається код конкретної служби, зареєстрований у журналі подій. Це значення дорівнює значенню, визначеному [win32setserviceexitcode()](function.win32-set-service-exit-code.html)

`CheckPoint`

Якщо служба завершила роботу, відображається поточний номер контрольної точки. Це використовується SCM як свого роду серцебиття для виявлення процесу обслуговування, що заклинив. Значення контрольної точки найкраще інтерпретувати разом із значенням WaitHint.

`WaitHint`

Якщо служба завершила роботу, вона встановить для WaitHint значення контрольної точки, яка вказуватиме на 100% завершення. Це можна використовувати для реалізації індикатора прогресу.

`ProcessId`

Ідентифікатор Windows. Якщо 0, процес не запущено.

`ServiceFlags`

dwServiceFlags. Дивіться [Константы флагов службы Win32Service](win32service.constants.serviceflag.html)

### Помилки

Викидається [ValueError](class.valueerror.html), якщо значення параметра `servicename` не вказано.

### список змін

| Версия                  | Описание                                                                                                                                                              |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.html) у разі невірних даних у параметрах раніше поверталося **`false`**                                                         |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.html) у разі виникнення помилки, раніше повертався [Код ошибки Win32](win32service.constants.errors.html) |
| PECL win32service 1.0.0 | Тип повернення тепер array, раніше був [mixed](language.types.declarations.html#language.types.declarations.mixed)                                                    |

### Дивіться також

-   [Предопределённые константы Win32Service](win32service.constants.html)