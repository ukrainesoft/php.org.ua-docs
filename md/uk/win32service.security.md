Питання безпеки

-   [« Типы ресурсов](win32service.resources.html)
    
-   [Предопределённые константы »](win32service.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](win32service.setup.html)
    
-   Питання безпеки
    

## Питання безпеки

Цьому модулю необхідні права адміністратора для здійснення таких дій як: [create](function.win32-create-service.html) [delete](function.win32-delete-service.html) [start](function.win32-start-service.html) [stop](function.win32-stop-service.html) [pause](function.win32-pause-service.html) і [continue](function.win32-continue-service.html). Ця вимога може викликати підвищення привілеїв, якщо керування службами доступне через веб-інтерфейс або дистанційне керування.

Ви можете встановити ACL для сервісу після його додавання до SCM для делегування адміністративних завдань не адміністраторському обліковому запису, або обліковому запису сервісу. Детальніше читайте в [» Microsoft Knowledge Base](https://support.microsoft.com/en-us/help/914392/best-practices-and-guidance-for-writers-of-service-discretionary-acces)