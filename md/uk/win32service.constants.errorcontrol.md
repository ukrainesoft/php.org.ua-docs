- [« Константи типу запуску служби Win32Service](win32service.constants.servicestarttype.md)
- [Константи прапорів сервісу Win32Service »](win32service.constants.serviceflag.md)

- [PHP Manual](index.md)
- [Предвизначені константи](win32service.constants.md)
- Константи контролю помилок сервісу Win32Service

| Константа Значення               | Опис       |
| -------------------------------- | ---------- |
| **WIN32_SERVICE_ERROR_IGNORE**   | 0x00000000 | Програма, що запускається, ігнорує помилки і продовжує запускатися. |            
| **WIN32_SERVICE_ERROR_NORMAL**   | 0x00000001 | Програма записує помилку в журнал помилок, але продовжує запускатися.
| **WIN32_SERVICE_ERROR_SEVERE**   | 0x00000002 | Записувати помилки старту програми до журналу подій. Якщо запускається остання відома хороша конфігурація, процес запуску продовжиться. Інакше система перезапуститься з останньою відомою гарною конфігурацією.
| **WIN32_SERVICE_ERROR_CRITICAL** | 0x00000003 | Записувати помилки старту програми в лог подій, якщо це можливо. Якщо запускається остання відома хороша конфігурація, процес запуску припиниться. Інакше система перезапуститься з останньою відомою гарною конфігурацією.

**Константи контролю помилок сервісу Win32Service**
