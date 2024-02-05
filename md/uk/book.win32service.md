---
navigation:
  - function.variant-xor.md: « variant\_xor
  - intro.win32service.md: Вступ "
  - index.md: PHP Manual
  - refs.utilspec.windows.md: Модулі лише для Windows
title: win32service
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32service

-   [Вступ](intro.win32service.md)
-   [Встановлення та налаштування](win32service.setup.md)
    -   [Вимоги](win32service.requirements.md)
    -   [Установка](win32service.installation.md)
    -   [Налаштування під час виконання](win32service.configuration.md)
    -   [Типи ресурсів](win32service.resources.md)
    -   [Питання безпеки](win32service.security.md)
-   [Обумовлені константи](win32service.constants.md)
    -   [Побутові маски типу служби Win32Service](win32service.constants.servicetype.md)
    -   [Константи статусу служби Win32Service](win32service.constants.servicestatus.md)
    -   [Константи обробки повідомлень службою Win32Service](win32service.constants.servicecontrol.md)
    -   [Приймаються бітові маски обробки повідомлень службою Win32Service](win32service.constants.controlsaccepted.md)
    -   [Константи типу запуску служби Win32Service](win32service.constants.servicestarttype.md)
    -   [Константи контролю помилок сервісу Win32Service](win32service.constants.errorcontrol.md)
    -   [Константи прапорів сервісу Win32Service](win32service.constants.serviceflag.md)
    -   [Коди помилок Win32](win32service.constants.errors.md)
    -   [Базові класи пріоритетів Win32](win32service.constants.basepriorities.md)
    -   [Дії відновлення Win32](win32service.constants.recovery-action.md)
    -   [Win32 Service informations](win32service.constants.serviceinfos.md)
-   [Win32ServiceException](class.win32serviceexception.md) \- Клас Win32ServiceException
-   [Приклади](win32service.examples.md)
-   [win32service](ref.win32service.md)
    -   [win32\_continue\_service](function.win32-continue-service.md)— Відновлює роботу зупиненої служби
    -   [win32\_create\_service](function.win32-create-service.md)— Створює новий запис служби у базі даних SCM
    -   [win32\_delete\_service](function.win32-delete-service.md)— Видалення запису служби з бази даних SCM
    -   [win32\_get\_last\_control\_message](function.win32-get-last-control-message.md)— Повертає останнє повідомлення керування, яке було надіслано цій службі
    -   [win32\_pause\_service](function.win32-pause-service.md) \- Припиняє службу
    -   [win32\_query\_service\_status](function.win32-query-service-status.md)— Запитує статус сервісу
    -   [win32\_send\_custom\_control](function.win32-send-custom-control.md)— Відправляє елемент керування, що настроюється, до служби
    -   [win32\_set\_service\_exit\_code](function.win32-set-service-exit-code.md)— Визначає або повертає вихідний код для поточної запущеної служби
    -   [win32\_set\_service\_exit\_mode](function.win32-set-service-exit-mode.md)— Визначає або повертає вихідний режим для поточної запущеної служби
    -   [win32\_set\_service\_status](function.win32-set-service-status.md)— Оновлює статус служби
    -   [win32\_start\_service\_ctrl\_dispatcher](function.win32-start-service-ctrl-dispatcher.md)— Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям
    -   [win32\_start\_service](function.win32-start-service.md) \- Запускає службу
    -   [win32\_stop\_service](function.win32-stop-service.md) \- Зупиняє службу
