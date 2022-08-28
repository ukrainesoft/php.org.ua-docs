Константи типу запуску служби Win32Service

-   [« Принимаемые битовые маски обработки сообщений службой Win32Service](win32service.constants.controlsaccepted.html)
    
-   [Константы контроля ошибок сервиса Win32Service »](win32service.constants.errorcontrol.html)
    
-   [PHP Manual](index.html)
    
-   [Предопределённые константы](win32service.constants.html)
    
-   Константи типу запуску служби Win32Service
    

**Константи типу запуску служби Win32Service**

| Константа | Значение | Описание |
| --- | --- | --- |
| **`WIN32_SERVICE_BOOT_START`** | 0x00000000 | Драйвер пристрою запускається системним завантажувачем. Це значення коректне лише для драйверів. |
| **`WIN32_SERVICE_SYSTEM_START`** | 0x00000001 | Драйвер пристрою запускається функцією IoInitSystem. Це значення коректне лише для драйверів. |
| **`WIN32_SERVICE_AUTO_START`** | 0x00000002 | Служба запускається автоматично під час запуску системи. |
| **`WIN32_SERVICE_DEMAND_START`** | 0x00000003 | Сервіс стартує автоматично, якщо будь-який процес викликав функцію StartService. |
| **`WIN32_SERVICE_DISABLED`** | 0x00000004 | Сервіс не може бути запущений. Спроба його старту викликає помилку **`WIN32_ERROR_SERVICE_DISABLED`** |