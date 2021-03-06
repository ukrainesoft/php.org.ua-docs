- [« Константи обробки повідомлень службою Win32Service](win32service.constants.servicecontrol.md)
- [Константи типу запуску служби Win32Service »](win32service.constants.servicestarttype.md)

- [PHP Manual](index.md)
- [Предвизначені константи](win32service.constants.md)
- Приймаються бітові маски обробки повідомлень службою Win32Service

| Константа Значення                             | Опис       |
| ---------------------------------------------- | ---------- |
| **WIN32_SERVICE_ACCEPT_HARDWAREPROFILECHANGE** | 0x00000020 | Сервіс повідомлено про те, що апаратна конфігурація комп'ютера змінена. Це дозволяє системі надіслати службі повідомлення **WIN32_SERVICE_CONTROL_HARDWAREPROFILECHANGE**. |            
| **WIN32_SERVICE_ACCEPT_NETBINDCHANGE**         | 0x00000010 | Служба - це мережевий компонент, який приймає зміни у своїй прив'язці без необхідності зупинення та перезапуску. Цей керуючий прапор дозволяє службі приймати такі повідомлення: **WIN32_SERVICE_CONTROL_NETBINDADD**, **WIN32_SERVICE_CONTROL_NETBINDREMOVE**, **WIN32_SERVICE_CONTROL_NETBINDENABLE** та **WIN32_SERV.
| **WIN32_SERVICE_ACCEPT_PARAMCHANGE**           | 0x00000008 | Служба може перечитати стартові параметри без необхідності зупинки та перезапуску. Цей прапор, що управляє, дозволяє службі приймати наступні повідомлення: **WIN32_SERVICE_CONTROL_PARAMCHANGE**.
| **WIN32_SERVICE_ACCEPT_PAUSE_CONTINUE**        | 0x00000002 | Служба може бути припинена та продовжена. Цей код дозволяє службі приймати повідомлення **WIN32_SERVICE_CONTROL_PAUSE** та **WIN32_SERVICE_CONTROL_CONTINUE**.
| **WIN32_SERVICE_ACCEPT_POWEREVENT**            | 0x00000040 | Служба повідомляється, коли змінився статус електропостачання. Дозволяє системі надсилати службі повідомлення **WIN32_SERVICE_CONTROL_POWEREVENT**.
| **WIN32_SERVICE_ACCEPT_PRESHUTDOWN**           | 0x00000100 | Служба може виконувати завдання під час зупинки системи. Цей код дозволяє службі приймати повідомлення **WIN32_SERVICE_CONTROL_PRESHUTDOWN**. Це значення не підтримується Windows Server 2003 та Windows XP/2000.
| **WIN32_SERVICE_ACCEPT_SESSIONCHANGE**         | 0x00000080 | Сервіс сповіщається, коли змінився статус сесії на комп'ютері. Дозволяє системі надсилати службі повідомлення **WIN32_SERVICE_CONTROL_SESSIONCHANGE**. Не підтримується Windows 2000
| **WIN32_SERVICE_ACCEPT_SHUTDOWN**              | 0x00000004 | Служба має бути сповіщена, що система зупиняється. Цей код дозволяє службі приймати повідомлення **WIN32_SERVICE_CONTROL_SHUTDOWN**.
| **WIN32_SERVICE_ACCEPT_STOP**                  | 0x00000001 | Ця служба може бути зупинена. Цей код дозволяє службі приймати повідомлення **WIN32_SERVICE_CONTROL_STOP**.
| **WIN32_SERVICE_ACCEPT_TIMECHANGE**            | 0x00000200 | Служба повідомляється, коли змінився системний час. Дозволяє системі надсилати службі оповіщення **WIN32_SERVICE_CONTROL_TIMECHANGE**. У Windows Server 2008, Windows Vista, Windows Server 2003 та Windows XP/2000 цей керуючий код не використовується.
| **WIN32_SERVICE_ACCEPT_TRIGGEREVENT**          | 0x00000400 | Служба повідомляється, коли відбувається подія, для якої вона зареєстрована. Дозволяє системі надсилати службі оповіщення **WIN32_SERVICE_CONTROL_TRIGGEREVENT**. У Windows Server 2008, Windows Vista, Windows Server 2003 та Windows XP/2000 цей керуючий код не використовується.

**Приймаються бітові маски обробки повідомлень службою Win32Service**
