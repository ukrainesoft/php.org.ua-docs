---
navigation:
  - info.resources.md: « Типи ресурсів
  - ref.info.md: Опції PHP/інформаційні функції »
  - index.md: PHP Manual
  - book.info.md: Опції/інформація PHP
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи завжди доступні як частина ядра PHP.

**Обумовлені константи [phpcredits()](function.phpcredits.md)**

| Константы | Значение | Опис |
| --- | --- | --- |
| **`CREDITS_GROUP`** |  | Список розробників ядра PHP |
| **`CREDITS_GENERAL`** |  | Головні розробники: Дизайн та концепції мови, автори PHP та модуля SAPI. |
| **`CREDITS_SAPI`** | 4 | Список серверних API для PHP та їх автори. |
| **`CREDITS_MODULES`** | 8 | Список модулів для PHP та їх автори. |
| **`CREDITS_DOCS`** | 16 | Члени команди розробників документації. |
| **`CREDITS_FULLPAGE`** | 32 | Часто вказують у поєднанні з іншими прапорами. Означає, що HTML-сторінка повинна друкуватись разом із додатковою інформацією (за яку відповідають інші прапори). |
| **`CREDITS_QA`** | 64 | Члени команди контролю якості. |
| **`CREDITS_ALL`** | \- | Усі розробники, аналогічно до значення: `CREDITS_DOCS + CREDITS_GENERAL + CREDITS_GROUP + CREDITS_MODULES + CREDITS_QA CREDITS_FULLPAGE`. . Буде згенерована HTML-сторінка із заданими тегами. Це значення за промовчанням. |

**Константи [phpinfo()](function.phpinfo.md)**

| Константы | Значение | Опис |
| --- | --- | --- |
| **`INFO_GENERAL`** |  | Рядок конфігурації, розташування файлу php.ini, дата складання, веб-сервер, система та ін. |
| **`INFO_CREDITS`** |  | Розробники PHP. Дивіться також [phpcredits()](function.phpcredits.md) |
| **`INFO_CONFIGURATION`** | 4 | Поточні локальні та основні значення директив PHP. Дивіться також [ini\_get()](function.ini-get.md) |
| **`INFO_MODULES`** | 8 | Завантажені модулі та їх налаштування. |
| **`INFO_ENVIRONMENT`** | 16 | Інформація про змінні середовища, яка також доступна в [$\_ENV](reserved.variables.environment.md) |
| **`INFO_VARIABLES`** | 32 | Показує все [зумовлені змінні](language.variables.predefined.md)из`EGPCS` (Environment, GET, POST, Cookie, Server). |
| **`INFO_LICENSE`** | 64 | Інформація про ліцензію PHP. Дивіться також "[» FAQ за ліцензією](https://www.php.net/license/)». |
| **`INFO_ALL`** | \- | Константа за замовчуванням. Показує всю інформацію, описану вище. |

**Константи режиму INI**

| Константы | Опис |
| --- | --- |
| **`INI_USER`**(int) | Запис задають у скриптах користувача (наприклад, функцією [ini\_set()](function.ini-set.md) [у реєстрі Windows](configuration.changes.md#configuration.changes.windows) або файлі .user.ini |
| **`INI_PERDIR`**(int) | Запис встановлюють у файлах php.ini, .htaccess, httpd.conf чи .user.ini |
| **`INI_SYSTEM`**(int) | Запис встановлюють у файлах php.ini або httpd.conf |
| **`INI_ALL`**(int) | Запис дозволено встановлювати будь-де |

Константи перевірки тверджень. Ці значення користуються, щоб задати налаштування через функцію [assert\_options()](function.assert-options.md)

**[assert()](function.assert.md) константи**

| Константы | INI настройка | Опис |
| --- | --- | --- |
| **`ASSERT_ACTIVE`** | [assert.active](info.configuration.md#ini.assert.active) | Увімкнення [assert()](function.assert.md) перевірок. |
| **Увага** |  |  |

Ця функціональність оголошена *застарілої* починаючи з PHP 8.3.0 і її украй не рекомендується використовувати.

**`ASSERT_CALLBACK`** [assert.callback](info.configuration.md#ini.assert.callback) | Зворотний дзвінок при провалі перевірки затвердження.

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 8.3.0 і її украй не рекомендується використовувати.

**`ASSERT_BAIL`** [assert.bail](info.configuration.md#ini.assert.bail) | Перервати виконання при провалі перевірки затвердження.

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 8.3.0 і її украй не рекомендується використовувати.

**`ASSERT_EXCEPTION`** [assert.exception](info.configuration.md#ini.assert.exception) | Видає попередження PHP для кожного невдалого затвердження.

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 8.3.0 і її украй не рекомендується використовувати.

**`ASSERT_WARNING`** [assert.warning](info.configuration.md#ini.assert.warning) | Видавати попередження PHP у разі провалу перевірки кожного затвердження

**Увага**

Ця функціональність оголошена *застарілої* починаючи з PHP 8.3.0 і її украй не рекомендується використовувати.

**`ASSERT_QUIET_EVAL`** [assert.quiet\_eval](info.configuration.md#ini.assert.quiet-eval) | Вимкнути `error_reporting` під час виконання перевірки затвердження.

**Увага**

Ця функціональність була *ВИДАЛЕНО* у PHP 8.0.0.

Наступні константи доступні лише в операційній системі Windows та повідомляють інформацію про версії програмного забезпечення.

**Специфічні для Windows константи**

| Константы | Опис |
| --- | --- |
| **`PHP_WINDOWS_VERSION_MAJOR`** | Основний номер версії Windows, можливі значення `4` (NT4/Me/98/95), `5` (XP/2003 R2/2003/2000) або `6` (Vista/2008/7/8/8.1). |
| **`PHP_WINDOWS_VERSION_MINOR`** | Уточнюючий номер версії Windows, можливі значення (Vista/2008/2000/NT4/95), (XP), (2003 R2/2003/XP x64), `10` (98) або `90` (ME). |
| **`PHP_WINDOWS_VERSION_BUILD`** | Номер збирання Windows (наприклад, у Windows Vista SP1 номер збирання 6001) |
| **`PHP_WINDOWS_VERSION_PLATFORM`** | Платформа, де працює PHP. Можливі значення для Windows Vista/XP/2000/NT4, Server 2008/2003, а для Windows ME/98/95 це значення буде |
| **`PHP_WINDOWS_VERSION_SP_MAJOR`** | Основний номер версії встановленого пакета сервісу. Можливе значення , якщо пакети не встановлені. Наприклад, у Windows XP із третім встановленим пакетом оновлення значення буде `3` |
| **`PHP_WINDOWS_VERSION_SP_MINOR`** | Додатковий номер встановленого пакета оновлень. Значення говорить про те, що пакети не встановлені. |
| **`PHP_WINDOWS_VERSION_SUITEMASK`** | Бітова маска, яка вказує, яка додаткова функціональність встановлена ​​у Windows. Нижче наведено таблицю з можливими значеннями бітового поля. |
| **`PHP_WINDOWS_VERSION_PRODUCTTYPE`** | Містить значення, що визначає константи виду `PHP_WINDOWS_NT_*`. . Значенням буває одна з констант `PHP_WINDOWS_NT_*`, що вказує на тип платформи. |
| **`PHP_WINDOWS_NT_DOMAIN_CONTROLLER`** | Контролер домену |
| **`PHP_WINDOWS_NT_SERVER`** | Серверна система (наприклад, Server 2008/2003/2000). Враховують, що якщо сервер — контролер домену, замість цієї константи видаватиметься **`PHP_WINDOWS_NT_DOMAIN_CONTROLLER`** |
| **`PHP_WINDOWS_NT_WORKSTATION`** | Система робочої станції (наприклад, Vista/XP/2000/NT4) |

Таблица значений битовой маски\*\*`PHP_WINDOWS_VERSION_SUITEMASK`\*\*

**Бітове поле функціональних можливостей Windows**

| Биты | Опис |
| --- | --- |
| `0x00000004` | Встановлено компоненти Microsoft BackOffice. |
| `0x00000400` | Встановлено Windows Server 2003 Web Edition. |
| `0x00004000` | Встановлено Windows Server 2003 Compute Cluster Edition. |
| `0x00000080` | Встановлено Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition або Windows 2000 Datacenter Server. |
| `0x00000002` | Встановлено Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, Windows 2000 Advanced Server або Windows NT Server 4.0 Enterprise Edition. |
| `0x00000040` | Встановлено Windows XP Embedded. |
| `0x00000200` | Встановлено Windows Vista Home Premium, Windows Vista Home Basic або Windows XP Home Edition. |
| `0x00000100` | Підтримується віддалений робочий стіл, але лише в інтерактивному режимі. Це значення встановлюється доти, доки система не буде запущена в режимі сервера програм. |
| `0x00000001` | Microsoft Small Business Server колись було встановлено в системі, але, можливо, було оновлено до іншої версії Windows. |
| `0x00000020` | Microsoft Small Business Server встановлено з обмеженою ліцензією. |
| `0x00002000` | Встановлено Windows Storage Server 2003 R2 або Windows Storage Server 2003. |
| `0x00000010` | Встановлено Служби терміналів. Це значення завжди встановлено. Якщо значення встановлено, але встановлено не значення `0x00000100`, система працює в режимі сервера додатків. |
| `0x00008000` | Встановлено Windows Home Server. |
