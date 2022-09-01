---
navigation:
  - info.resources.html: « Типи ресурсів
  - ref.info.html: Опції PHP/інформаційні функції »
  - index.html: PHP Manual
  - book.info.html: Опции/информация PHP
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи завжди доступні як частина ядра PHP.

**Обумовлені константи [phpcredits()](function.phpcredits.html)**

| Константа | Значение | Описание |
| --- | --- | --- |
| **`CREDITS_GROUP`** |  | Список розробників ядра PHP |
| **`CREDITS_GENERAL`** |  | Головні розробники: Дизайн та концепції мови, автори PHP та модуля SAPI. |
| **`CREDITS_SAPI`** |  | Список серверних API для PHP та їх автори. |
| **`CREDITS_MODULES`** |  | Список модулів для PHP та їх автори. |
| **`CREDITS_DOCS`** |  | Члени команди розробників документації. |
| **`CREDITS_FULLPAGE`** |  | Зазвичай використовується у поєднанні з іншими прапорами. Означає, що сторінка HTML повинна друкуватись разом з додатковою інформацією (за яку відповідають інші прапори). |
| **`CREDITS_QA`** |  | Члени команди контролю якості. |
| **`CREDITS_ALL`** |  | Усі розробники, аналогічно використанню: `CREDITS_DOCS + CREDITS_GENERAL + CREDITS_GROUP + CREDITS_MODULES + CREDITS_QA CREDITS_FULLPAGE`. Буде згенеровано HTML-сторінку з відповідними тегами. Це значення за промовчанням. |

**Константи [phpinfo()](function.phpinfo.html)**

| Константа | Значение | Описание |
| --- | --- | --- |
| **`INFO_GENERAL`** |  | Рядок конфігурації, розташування php.ini, дата складання, веб-сервер, система та ін. |
| **`INFO_CREDITS`** |  | Розробники PHP. Дивіться також [phpcredits()](function.phpcredits.html) |
| **`INFO_CONFIGURATION`** |  | Поточні локальні та основні значення директив PHP. Дивіться також [iniget()](function.ini-get.html) |
| **`INFO_MODULES`** |  | Завантажені модулі та їх налаштування. |
| **`INFO_ENVIRONMENT`** |  | Інформація про змінні середовища, яка також доступна в [ENV](reserved.variables.environment.html) |
| **`INFO_VARIABLES`** |  | Показує все [зумовлені змінні](language.variables.predefined.html) з `EGPCS` (Environment, GET, POST, Cookie, Server). |
| **`INFO_LICENSE`** |  | Інформація про ліцензію PHP. Дивіться також [» FAQ за ліцензією](https://www.php.net/license/) |
| **`INFO_ALL`** |  | Константа за замовчуванням. Показує всю інформацію, описану вище. |

**Константи INI**

| Константа | Значение | Описание |
| --- | --- | --- |
| `INI_USER` |  | Не використовується |
| `INI_PERDIR` |  | Не використовується |
| `INI_SYSTEM` |  | Не використовується |
| `INI_ALL` |  | Не використовується |

Константи перевірки тверджень. Ці значення використовуються для встановлення налаштувань [assertoptions()](function.assert-options.html)

**[assert()](function.assert.html) константи**

| Константа | INI настройка | Описание |
| --- | --- | --- |
| **`ASSERT_ACTIVE`** | assert.active | Увімкнення [assert()](function.assert.html) перевірок. |
| **`ASSERT_CALLBACK`** | assert.callback | Зворотний дзвінок при провалі перевірки затвердження. |
| **`ASSERT_BAIL`** | assert.bail | Перервати виконання при провалі перевірки затвердження. |
| **`ASSERT_WARNING`** | assert.warning | Видавати попередження PHP у разі провалу перевірки кожного затвердження |
| **`ASSERT_QUIET_EVAL`** | assert.quieteval | Вимкнути `error_reporting` під час виконання перевірки затвердження. Видалено, починаючи з PHP 8.0.0 |

Наступні константи доступні лише під Windows. Вони дозволяють отримати різноманітну інформацію про версії програмного забезпечення. Усі константи доступні з PHP 5.3.0.

**Специфічні для Windows константи**

| Константа | Описание |
| --- | --- |
| **`PHP_WINDOWS_VERSION_MAJOR`** | Основний номер версії Windows це може бути `4` (NT4/Me/98/95), `5` (XP/2003 R2/2003/2000) або `6` (Vista/2008/7/8/8.1). |
| **`PHP_WINDOWS_VERSION_MINOR`** | Уточнюючий номер версії Windows це може бути `0` (Vista/2008/2000/NT4/95), `1` (XP), `2` (2003 R2/2003/XP x64), `10` (98) або `90` (ME). |
| **`PHP_WINDOWS_VERSION_BUILD`** | Номер збирання Windows (наприклад, Windows Vista SP1 має номер збирання 6001) |
| **`PHP_WINDOWS_VERSION_PLATFORM`** | Платформа, на якій PHP працює зараз. Можливі значення `2` для Windows Vista/XP/2000/NT4, Server 2008/2003, а для Windows ME/98/95 це значення буде `1` |
| **`PHP_WINDOWS_VERSION_SP_MAJOR`** | Основний номер версії встановленого пакета сервісу. Можливе значення `0`, якщо пакети не встановлено. Наприклад, у Windows XP з 3м сервіс паком це значення буде `3` |
| **`PHP_WINDOWS_VERSION_SP_MINOR`** | Додатковий номер встановленого пакета оновлень. Значення `0` свідчить, що пакетів не встановлено. |
| **`PHP_WINDOWS_VERSION_SUITEMASK`** | Бітова маска, яка вказує, яка додаткова функціональність встановлена ​​в системі Windows. Нижче наведено таблицю з можливими значеннями бітового поля. |
| **`PHP_WINDOWS_VERSION_PRODUCTTYPE`** | Містить значення, що визначає константи виду `PHP_WINDOWS_NT_*`. Цим значенням може бути одна з констант `PHP_WINDOWS_NT_*` що вказує на тип платформи. |
| **`PHP_WINDOWS_NT_DOMAIN_CONTROLLER`** | Контролер домену |
| **`PHP_WINDOWS_NT_SERVER`** | Серверна система (наприклад, Server 2008/2003/2000). Потрібно врахувати, що якщо сервер є контролером домену, замість цієї константи видаватиметься **`PHP_WINDOWS_NT_DOMAIN_CONTROLLER`** |
| **`PHP_WINDOWS_NT_WORKSTATION`** | Система робочої станції (напр. Vista/XP/2000/NT4) |

Таблиця значень бітової маски **`PHP_WINDOWS_VERSION_SUITEMASK`**

**Бітове поле функціональних можливостей Windows**

| Биты | Описание |
| --- | --- |
| `0x00000004` | Встановлено компоненти Microsoft BackOffice. |
| `0x00000400` | Встановлено Windows Server 2003 Web Edition. |
| `0x00004000` | Встановлено Windows Server 2003 Compute Cluster Edition. |
| `0x00000080` | Встановлено Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition або Windows 2000 Datacenter Server. |
| `0x00000002` | Встановлено Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, Windows 2000 Advanced Server або Windows NT Server 4.0 Enterprise Edition. |
| `0x00000040` | Встановлено Windows XP Embedded. |
| `0x00000200` | Встановлено Windows Vista Home Premium, Windows Vista Home Basic або Windows XP Home Edition. |
| `0x00000100` | Підтримується віддалений робочий стіл, але лише в інтерактивному режимі. Це значення встановлюється доти, доки система не буде запущена в режимі сервера програм. |
| `0x00000001` | Microsoft Small Business Server було встановлено спочатку, проте міг бути проведений апгрейд системи до іншої версії Windows. |
| `0x00000020` | Microsoft Small Business Server встановлено з обмеженою ліцензією. |
| `0x00002000` | Встановлено Windows Storage Server 2003 R2 або Windows Storage Server 2003. |
| `0x00000010` | Встановлено термінальні служби. Це значення завжди встановлено. Якщо це значення встановлено, значення `0x00000100` не встановлено, система працює в режимі сервера додатків. |
| `0x00008000` | Встановлено Windows Home Server. |
