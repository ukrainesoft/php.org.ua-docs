---
navigation:
  - win32service.constants.controlsaccepted.md: '« бітові маски обробки повідомлень, що приймаються службою Win32Service'
  - win32service.constants.errorcontrol.md: Константи контролю помилок сервісу Win32Service
  - index.md: PHP Manual
  - win32service.constants.md: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
**Константи типу запуску служби Win32Service**

| Константа | Значение | Опис |
| --- | --- | --- |
| **`WIN32_SERVICE_BOOT_START`** | 0x00000000 | Драйвер пристрою запускається системним завантажувачем. Це значення коректне лише для драйверів. |
| **`WIN32_SERVICE_SYSTEM_START`** | 0x00000001 | Драйвер пристрою запускається функцією IoInitSystem. Це значення коректне лише для драйверів. |
| **`WIN32_SERVICE_AUTO_START`** | 0x00000002 | Служба запускається автоматично під час запуску системи. |
| **`WIN32_SERVICE_DEMAND_START`** | 0x00000003 | Сервіс стартує автоматично, якщо будь-який процес викликав функцію StartService. |
| **`WIN32_SERVICE_DISABLED`** | 0x00000004 | Сервіс не може бути запущений. Спроба його старту викликає помилку **`WIN32_ERROR_SERVICE_DISABLED`** |
