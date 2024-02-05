---
navigation:
  - win32service.resources.md: « Типи ресурсів
  - win32service.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - win32service.setup.md: Встановлення та налаштування
title: Питання безпеки
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Питання безпеки

Цьому модулю необхідні права адміністратора для здійснення таких дій, як: [create](function.win32-create-service.md) [delete](function.win32-delete-service.md) [start](function.win32-start-service.md) [stop](function.win32-stop-service.md) [pause](function.win32-pause-service.md) і [continue](function.win32-continue-service.md). Ця вимога може викликати підвищення привілеїв, якщо керування службами доступне через веб-інтерфейс або дистанційне керування.

Ви можете встановити ACL для сервісу після його додавання до SCM для делегування адміністративних завдань не адміністраторському обліковому запису, або обліковому запису сервісу. Детальніше читайте в [» Microsoft Knowledge Base](https://support.microsoft.com/en-us/help/914392/best-practices-and-guidance-for-writers-of-service-discretionary-acces)
