---
navigation:
  - function.win32-pause-service.md: « win32\_pause\_service
  - function.win32-send-custom-control.md: win32\_send\_custom\_control »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_query\_service\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_query\_service\_status

(PECL win32service >=0.1.0)

win32\_query\_service\_status — Запитує статус сервісу

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

До версії 1.0.0 **`false`** якщо була виявлена ​​проблема з параметрами або [код помилки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

`ServiceType`

dwServiceType. Смотрите[Побутові маски типів служби Win32Service](win32service.constants.servicetype.md)

`CurrentState`

dwCurrentState. Смотрите[Константи стану служби Win32Service](win32service.constants.servicestatus.md)

`ControlsAccepted`

Які елементи керування службами приймаються службою. Дивіться [Побутові маски Win32Service Service Control Message Accepted](win32service.constants.controlsaccepted.md)

`Win32ExitCode`

Якщо служба завершила роботу, тут з'являється код повернення з процесу. Це значення дорівнює \*\*`WIN32_ERROR_SERVICE_SPECIFIC_ERROR`\*\*якщо режим виходу не є плавним. Дивіться [коди помилок Win32Service](win32service.constants.errors.md) і [win32\_set\_service\_exit\_mode()](function.win32-set-service-exit-mode.md)

`ServiceSpecificExitCode`

Якщо служба завершила роботу, тут відображається код конкретної служби, зареєстрований у журналі подій. Це значення дорівнює значенню, визначеному [win32\_set\_service\_exit\_code()](function.win32-set-service-exit-code.md)

`CheckPoint`

Якщо служба завершила роботу, відображається поточний номер контрольної точки. Це використовується SCM як свого роду серцебиття для виявлення процесу обслуговування, що заклинив. Значення контрольної точки найкраще інтерпретувати разом із значенням WaitHint.

`WaitHint`

Якщо служба завершила роботу, вона встановить для WaitHint значення контрольної точки, яке вказуватиме на 100% завершення. Це можна використовувати для реалізації індикатора прогресу.

`ProcessId`

Ідентифікатор Windows. Якщо 0, процес не запущено.

`ServiceFlags`

dwServiceFlags. Смотрите[Константи прапорів служби Win32Service](win32service.constants.serviceflag.md)

### Помилки

Викидається [ValueError](class.valueerror.md), если значение параметра`servicename` не вказано.

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) у разі невірних даних у параметрах раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип повернення тепер array, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |

### Дивіться також

-   [Обумовлені константи Win32Service](win32service.constants.md)
