---
navigation:
  - function.win32-set-service-status.md: « win32\_set\_service\_status
  - function.win32-start-service.md: win32\_start\_service »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_start\_service\_ctrl\_dispatcher
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_start\_service\_ctrl\_dispatcher

(PECL win32service >=0.1.0)

win32\_start\_service\_ctrl\_dispatcher — Додає до Диспетчера служб скрипт, який може бути використаний, як служба із заданим ім'ям

### Опис

```methodsynopsis
win32_start_service_ctrl_dispatcher(string $name, bool $gracefulMode = true): void
```

При запуску за допомогою диспетчера служб, процесу служби необхідно звірятися з ним для моніторингу служби та зв'язку з нею. Ця функція виконує звіряння шляхом створення потоку для обробки низькорівневого зв'язку з диспетчером служб.

Після запуску процес служби має здійснити дві дії. Перше – повідомити диспетчеру служб, що службу запущено. Це здійснюється шляхом виклику [win32\_set\_service\_status()](function.win32-set-service-status.md) з константою **`WIN32_SERVICE_RUNNING`**. Якщо вам необхідно виконати тривалий процес перед запуском служби, то ви можете використовувати константу **`WIN32_SERVICE_START_PENDING`**. Друге – продовжити звіряння з диспетчером служб, щоб визначити необхідність відключення. Це здійснюється за допомогою періодичного виклику [win32\_get\_last\_control\_message()](function.win32-get-last-control-message.md)и обработки кода возврата соответствующим образом.

**Застереження**

Починаючи з версії 0.2.0, ця функція працює лише у "cli" SAPI. В інших SAPI функцію вимкнено.

### Список параметрів

`name`

Коротке ім'я служби, як при додаванні за допомогою [win32\_create\_service()](function.win32-create-service.md)

`gracefulMode`

**`true`** для "елегантного" виходу. . **`false`** для виходу із помилкою. Дивіться [win32\_set\_service\_exit\_mode()](function.win32-set-service-exit-mode.md) для отримання детальної інформації.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код помилки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

До версії 1.0.0, якщо SAPI не є `"cli"`, дана функція викликає помилку рівня **`E_ERROR`**

Починаючи з версії 1.0.0, викидає виняток [Win32ServiceException](class.win32serviceexception.md), якщо SAPI не є `"cli"`

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) при некоректних даних у параметрах, що раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип значення, що повертається void, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |
| PECL win32service 0.4.0 | Добавлен параметр`gracefulMode` |
| PECL win32service 0.2.0 | Ця функція працює тільки з `"cli"`SAPI. |

### Приклади

**Приклад #1 Приклад**win32\_start\_service\_ctrl\_dispatcher()\*\*\*\*

Перевірте, чи запущено сервіс у диспетчері служб.

```php
<?php
if (!win32_start_service_ctrl_dispatcher('dummyphp')) {

  die("Я, вероятно, не запущен в диспетчере служб");
}

win32_set_service_status(WIN32_SERVICE_START_PENDING);

// Некий длительный процесс для обработки и запуска службы.

win32_set_service_status(WIN32_SERVICE_RUNNING);

while (WIN32_SERVICE_CONTROL_STOP != win32_get_last_control_message()) {
  # здесь производятся какие-то действия, не занимающие больше чем 30 секунд
  # перед соответствующим переходом в цикл.
}
?>
```

### Дивіться також

-   [win32\_set\_service\_status()](function.win32-set-service-status.md) \- Оновлює статус служби
-   [win32\_get\_last\_control\_message()](function.win32-get-last-control-message.md) \- Повертає останнє керуюче повідомлення, яке було надіслано цій службі
-   [win32\_set\_service\_exit\_mode()](function.win32-set-service-exit-mode.md) \- Визначає або повертає режим виходу для поточної запущеної служби
-   [win32\_set\_service\_exit\_code()](function.win32-set-service-exit-code.md) \- Визначає чи повертає код виходу для поточної запущеної служби
-   [Коди Помилок Win32](win32service.constants.errors.md)
