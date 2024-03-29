---
navigation:
  - function.win32-continue-service.md: « win32\_continue\_service
  - function.win32-delete-service.md: win32\_delete\_service »
  - index.md: PHP Manual
  - ref.win32service.md: win32service
title: win32\_create\_service
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# win32\_create\_service

(PECL win32service >=0.1.0)

win32\_create\_service — Створює новий запис служби у базі даних SCM

### Опис

```methodsynopsis
win32_create_service(array $details, string $machine = ?): void
```

Спробує додати службу до бази даних SCM. Для цього потрібні права адміністратора.

### Список параметрів

`details`

Масив деталей служби:

`service`

Коротка назва служби. Це ім'я, яке ви будете використовувати для керування службою за допомогою команди `net`. Служба повинна бути унікальною (ніякі дві служби не можуть мати одну й ту саму назву) і, в ідеалі, не повинна містити прогалин у назві.

`display`

Ім'я служби, що відображається. Це ім'я, яке ви побачите в аплеті служб.

`description`

Детальний опис послуги. Це опис, який ви побачите в аплеті служб.

`user`

Ім'я облікового запису користувача, під яким потрібно запускати службу. Якщо цей параметр не вказано, служба буде працювати під обліковим записом LocalSystem. Якщо вказано ім'я користувача, ви також повинні вказати пароль.

`password`

Пароль, соответствующий`user`

`path`

Повний шлях до модуля, який буде запущений при запуску служби. Якщо не вказано, використовуватиметься шлях до поточного процесу PHP.

`params`

Параметри командного рядка передачі службі під час її запуску. Якщо ви хочете запустити скрипт PHP як службу, то першим параметром має бути повний шлях до скрипту PHP, який ви збираєтеся запустити. Якщо ім'я скрипта або шлях містять прогалини, увімкніть повний шлях до скрипту в лапки `"`

`load_order`

Керує load\_order. Ще не повністю підтримується.

`svc_type`

Встановлює тип служби. Якщо опущено, буде використано значення за замовчуванням **`WIN32_SERVICE_WIN32_OWN_PROCESS`**. Не змінюйте цього, якщо ви не знаєте, що робите.

`start_type`

Встановлює спосіб запуску служби. За замовчуванням використовується **`WIN32_SERVICE_AUTO_START`**, що означає, що служба буде запущена під час запуску машини.

`error_control`

Повідомляє SCM, що він повинен робити при виявленні проблеми зі службою. За умовчанням це **`WIN32_SERVER_ERROR_IGNORE`**. Зміна цього значення поки що підтримується не повністю.

`delayed_start`

Якщо для `delayed_start`установлено значение\*\*`true`\*\*, Це проінформує SCM про те, що служба повинна бути запущена після того, як будуть запущені інші служби автозапуску, плюс невелика затримка.

Будь-яку службу можна позначити як службу з відкладеним автозапуском; однак цей параметр не діє, якщо `start_type` служби не дорівнює **`WIN32_SERVICE_AUTO_START`**

Параметр застосовується лише у Windows Vista та Windows Server 2008 або пізніших версіях.

`base_priority`

Щоб зменшити вплив на використання процесора, може знадобитися встановити базовий пріоритет нижче звичайного.

`base_priority` може бути однією з констант визначених у [базових класах пріоритету Win32](win32service.constants.basepriorities.md)

`dependencies`

Щоб визначити залежність вашої служби, може знадобитися встановити цей параметр для списку імен служб у масиві.

`recovery_delay`

Цей параметр визначає затримку між помилкою та виконанням дії відновлення. Значення у мілісекундах.

Значення за замовчуванням – 60000.

`recovery_action_1`

Дія буде виконана за першої помилки. Значення за замовчуванням - **`WIN32_SC_ACTION_NONE`**

Для`recovery_action_1` можна задати одну з констант [дій відновлення Win32](win32service.constants.recovery-action.md)

`recovery_action_2`

Дія буде виконана за другої помилки. Значення за замовчуванням - **`WIN32_SC_ACTION_NONE`**

Для`recovery_action_2` можна задати одну з констант [дій відновлення Win32](win32service.constants.recovery-action.md)

`recovery_action_3`

Дія буде виконана за наступних помилок. Значення за замовчуванням - **`WIN32_SC_ACTION_NONE`**

Для`recovery_action_3` можна задати одну з констант [дій відновлення Win32](win32service.constants.recovery-action.md)

`recovery_reset_period`

Лічильник відмов буде скинутий після затримки, визначеної у параметрі. Затримка вказується за секунди.

Значение по умолчанию`86400`

`recovery_enabled`

Встановіть для цього параметра значення \*\*`true`**для включения настроек восстановления,**`false`\*\*для отключения.

Значение по умолчанию\*\*`false`\*\*

`recovery_reboot_msg`

Встановіть цей параметр, щоб визначити повідомлення, яке зберігається в журналі подій Windows перед перезавантаженням. Використовується, лише якщо для однієї з дій встановлено значення **`WIN32_SC_ACTION_REBOOT`**

`recovery_command`

Встановіть цей параметр, щоб визначити команду, яка виконується, якщо одна з дій визначена, як **`WIN32_SC_ACTION_RUN_COMMAND`**

`machine`

Необов'язкове ім'я машини, на якій потрібно створити службу. Якщо не вказано, використовуватиметься локальний комп'ютер.

### Значення, що повертаються

Функція не повертає значення після виконання.

До версії 1.0.0, Повертає **`WIN32_NO_ERROR`** у разі успішного завершення **`false`** якщо була виявлена ​​проблема з параметрами або [код помилки Win32](win32service.constants.errors.md) при невдалому завершенні роботи.

### Помилки

Викидається [ValueError](class.valueerror.md), если значение параметра`service`не задано.

Викидається [ValueError](class.valueerror.md), если значение параметра`path`не задано.

Викидається [ValueError](class.valueerror.md), если значение параметра`svc_type` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`start_type` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`error_control` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`base_priority` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`recovery_delay` не в проміжку між 0 та PHP\_INT\_MAX.

Викидається [ValueError](class.valueerror.md), если значение параметра`recovery_action_1` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`recovery_action_2` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`recovery_action_3` вказано неправильно.

Викидається [ValueError](class.valueerror.md), если значение параметра`recovery_reset_period` не в проміжку між 0 та PHP\_INT\_MAX.

У разі виникнення помилки викидається [Win32ServiceException](class.win32serviceexception.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL win32service 1.0.0 | Викидає [ValueError](class.valueerror.md) у разі невірних даних у параметрах раніше поверталося **`false`** |
| PECL win32service 1.0.0 | Викидає [Win32ServiceException](class.win32serviceexception.md) у разі виникнення помилки, раніше повертався [Код помилки Win32](win32service.constants.errors.md) |
| PECL win32service 1.0.0 | Тип повернення тепер void, раніше був [mixed](language.types.declarations.md#language.types.declarations.mixed) |
| PECL win32service 0.4.0 | Додані параметри `dependencies` `recovery_delay` `recovery_action_1` `recovery_action_2` `recovery_action_3` `recovery_reset_period` `recovery_enabled` `recovery_reboot_msg`и`recovery_command` |

### Приклади

**Приклад #1 Приклад використання** win32\_create\_service()\*\*\*\*

Створення сервісу з короткою назвою dummyphp.

```php
<?php
$x = win32_create_service(array(
    'service'     => 'dummyphp',                                           // название сервиса
    'display'     => 'sample dummy PHP service',                           // краткое описание
    'description' => 'This is a dummy Windows service created using PHP.', // полное описание
    'params'      => '"' . __FILE__ . '"  run',                            // путь до скрипта и параметров
));
debug_zval_dump($x);
?>
```

**Приклад #2 Приклад використання** win32\_create\_service()\*\* із залежностями\*\*

Створення сервісу з короткою назвою 'dummyphp' та залежностями.

```php
<?php
$x = win32_create_service(array(
    'service'      => 'dummyphp',                                           // название сервиса
    'display'      => 'sample dummy PHP service',                           // краткое описание
    'description'  => 'This is a dummy Windows service created using PHP.', // полное описание
    'params'       => '"' . __FILE__ . '"  run',                            // путь до скрипта и параметров
    'dependencies' => array("Netman"),                                      // список зависимостей
));
debug_zval_dump($x);
?>
```

**Приклад #3 Приклад використання** win32\_create\_service()**с восстановлением**

Створення сервісу з короткою назвою 'dummyphp' та налаштуваннями відновлення.

```php
<?php
$x = win32_create_service(array(
    'service'               => 'dummyphp',                                           // название сервиса
    'display'               => 'sample dummy PHP service',                           // краткое описание
    'description'           => 'This is a dummy Windows service created using PHP.', // полное описание
    'params'                => '"' . __FILE__ . '"  run',                            // путь до скрипта и параметров
    'recovery_delay'        => 120000,                                               // Действие восстановления выполняется через 2 минуты.
    'recovery_action_1'     => WIN32_SC_ACTION_RESTART,                              // При первом сбое перезапускается служба.
    'recovery_action_2'     => WIN32_SC_ACTION_RUN_COMMAND,                          // При втором сбое выполняется команда
    'recovery_action_3'     => WIN32_SC_ACTION_NONE,                                 // При последующих сбоях ничего не делать
    'recovery_reset_period' => 86400,                                                // Сбросить счётчик ошибок через 1 день
    'recovery_enabled'      => true,                                                 // Включить параметр восстановления
    'recovery_reboot_msg'   => null,                                                 // Не определяйте сообщение о перезагрузке, здесь оно не нужно
    'recovery_command'      => "c:\clean-service.bat",                               // Когда действие - WIN32_SC_ACTION_RUN_COMMAND, выполняется эта команда
));
debug_zval_dump($x);
?>
```

### Дивіться також

-   [win32\_delete\_service()](function.win32-delete-service.md) \- Видалення запису служби з бази даних SCM
-   [Базові класи пріоритету Win32](win32service.constants.basepriorities.md)
-   [Дії відновлення Win32](win32service.constants.recovery-action.md)
-   [Коди помилок Win32](win32service.constants.errors.md)
