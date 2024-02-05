---
navigation:
  - seaslog.installation.md: « Встановлення
  - seaslog.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - seaslog.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Seaslog**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [seaslog.appender](seaslog.configuration.md#ini.seaslog.appender) |  | **`INI_SYSTEM`** |  |
| [seaslog.appender\_retry](seaslog.configuration.md#ini.seaslog.appender-retry) |  | **`INI_ALL`** |  |
| [seaslog.level](seaslog.configuration.md#ini.seaslog.level) | 8 | **`INI_ALL`** |  |
| [seaslog.remote\_host](seaslog.configuration.md#ini.seaslog.remote-host) | 127.0.0.1 | **`INI_ALL`** |  |
| [seaslog.remote\_port](seaslog.configuration.md#ini.seaslog.remote-port) | 514 | **`INI_ALL`** |  |
| [seaslog.remote\_timeout](seaslog.configuration.md#ini.seaslog.remote-timeout) |  | **`INI_SYSTEM`** |  |
| [seaslog.default\_basepath](seaslog.configuration.md#ini.seaslog.default-basepath) | /var/log/www | **`INI_SYSTEM`** |  |
| [seaslog.default\_logger](seaslog.configuration.md#ini.seaslog.default-logger) | default | **`INI_SYSTEM`** |  |
| [seaslog.default\_template](seaslog.configuration.md#ini.seaslog.default-template) | %T | %L | %P |
| [seaslog.default\_datetime\_format](seaslog.configuration.md#ini.seaslog.default-datetime-format) | Y-m-d H:i:s | **`INI_SYSTEM`** |  |
| [seaslog.trace\_error](seaslog.configuration.md#ini.seaslog.trace-error) |  | **`INI_ALL`** |  |
| [seaslog.trace\_exception](seaslog.configuration.md#ini.seaslog.trace-exception) |  | **`INI_SYSTEM`** |  |
| [seaslog.trace\_notice](seaslog.configuration.md#ini.seaslog.trace-notice) |  | **`INI_ALL`** |  |
| [seaslog.trace\_warning](seaslog.configuration.md#ini.seaslog.trace-warning) |  | **`INI_ALL`** |  |
| [seaslog.use\_buffer](seaslog.configuration.md#ini.seaslog.use-buffer) |  | **`INI_SYSTEM`** |  |
| [seaslog.buffer\_size](seaslog.configuration.md#ini.seaslog.buffer-size) |  | **`INI_ALL`** |  |
| [seaslog.buffer\_disabled\_in\_cli](seaslog.configuration.md#ini.seaslog.buffer-disabled-in-cli) |  | **`INI_SYSTEM`** |  |
| [seaslog.disting\_type](seaslog.configuration.md#ini.seaslog.disting-type) |  | **`INI_SYSTEM`** |  |
| [seaslog.disting\_folder](seaslog.configuration.md#ini.seaslog.disting-folder) |  | **`INI_SYSTEM`** |  |
| [seaslog.disting\_by\_hour](seaslog.configuration.md#ini.seaslog.disting-by-hour) |  | **`INI_SYSTEM`** |  |
| [seaslog.recall\_depth](seaslog.configuration.md#ini.seaslog.recall-depth) |  | **`INI_ALL`** |  |
| [seaslog.trim\_wrap](seaslog.configuration.md#ini.seaslog.trim-wrap) |  | **`INI_ALL`** |  |
| [seaslog.ignore\_warning](seaslog.configuration.md#ini.seaslog.ignore-warning) |  | **`INI_ALL`** |  |
| [seaslog.throw\_exception](seaslog.configuration.md#ini.seaslog.throw-exception) |  | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`seaslog.appender`int

Перемикає сховище журналу записів. 1 – Файл, 2 – TCP, 3 – UDP (за замовчуванням 1)

SeasLog надішле журнал на сервер tcp://remote\_host:remote\_port або udp://remote\_host:remote\_port, якщо *seaslog.appender* налаштований на `2 (TCP)`или`3 (UDP)`

Когда*SeasLog* відправляє журнал TCP/UDP, стиль відповідає RFC5424 . `{logInfo}`, на який впливає *seaslog.default\_template*

```
Стиль журнала отформатирован следующим образом:
<15>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | DEBUG | 21423 | 599157af4e937 | 1466787583.322 | this is a neeke debug
<14>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | INFO | 21423 | 599157af4e937 | 1466787583.323 | this is a info log
<13>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | NOTICE | 21423 | 599157af4e937 | 1466787583.324 | this is a notice log
```

`seaslog.appender_retry`int

Записує кількість повторних спроб журналу. За замовчуванням 0 (не записує)

`seaslog.buffer_disabled_in_cli`int

Вимикає буфер у CLI. 1 - Так, 0 - Ні (за замовчуванням)

Увімкніть опцію buffer\_disabled\_in\_cli. buffer\_disabled\_in\_cli вимкнено за замовчуванням. Якщо увімкнути buffer\_disabled\_in\_cli і запустити його в CLI, параметр seaslog.use\_buffer буде скинутий, Seaslog НЕГАЙНО зробить запис у сховищі даних.

`seaslog.buffer_size`int

Вкажіть для параметра buffer\_значення size 100. Значення buffer\_за замовчуванням 0, це означає, що буфер не використовується. Якщо buffer\_size > 0, SeasLog перезапише дані у сховищі, якщо розмір попередньо записаного в пам'ять журналу >= buffer\_size та оновіть опитування пам'яті.

`seaslog.default_basepath`string

Базовий шлях журналу за промовчанням. За промовчанням "/var/log/www".

`seaslog.default_datetime_format`string

Стиль DateTime. За промовчанням "Y-m-d H:i:s".

`seaslog.default_logger`string

Шлях до реєстратора за замовчуванням. За промовчанням "default".

`seaslog.disting_by_hour`int

Перемикає режим реєстратора щогодини. 1 - Так, 0 - Ні (за замовчуванням)

> **Зауваження** :
> 
> *seaslog.disting\_by\_hour = 1* перемикає режим використання Logger DisTing щогодини. Це означає, що SeasLog буде створювати файл щогодини.

`seaslog.disting_folder`int

Перемикає режим використання реєстратора за папками. 1 - Так (за замовчуванням), 0 - Ні.

> **Зауваження** :
> 
> *seaslog.disting\_folder = 1* перемикає режим використання Logger DisTing за папками, це означає, що SeasLog буде створювати файли в папках і при цьому налаштуванні закриття SeasLog створить файл з підкресленням, використовуючи тип реєстратора та час, наприклад, default\_20180211.log.

`seaslog.disting_type`int

Перемикає режим використання реєстратора типу. 1 - Так, 0 - Ні (за замовчуванням)

> **Зауваження** :
> 
> *seaslog.disting\_type = 1* перемикає режим використання Logger DisTing за типом, це означає, що SeasLog створить файл info\\warn\\error чи іншого типу.

`seaslog.ignore_warning`int

Перемикає режим ігнорування попереджень SeasLog. 1 - Так (за замовчуванням), 0 - Ні.

> **Зауваження** :
> 
> *seaslog.ignore\_warning = 1* Відкриває попередження про ігнорування самого SeasLog. Коли права доступу до каталогу або порти сервера прийому заблоковані, вони ігноруються; під час закриття видається попередження.

`seaslog.level`int

Рівень запису реєстратора. Типово 8 (все). 0 - EMERGENCY, 1 - ALERT, 2 - CRITICAL, 3 - ERROR, 4 - WARNING, 5 - NOTICE, 6 - INFO, 7 - DEBUG, 8-ALL

> **Зауваження** :
> 
> Примітка: елемент конфігурації змінено, починаючи з версії 1.7.0. До версії 1.7.0, чим менше значення, тим більше записів ведеться відповідно до рівня: 0 - все, 1 - debug, 2 - info, 3-notice, 4-warning, 5-error, 6-critical, 7-alert 8-емергенці. До версії 1.7.0 значення за промовчанням - 0 (все).

`seaslog.recall_depth`int

Глибина виклику функції журналу. Буде торкнутися змінної `LineNo`в`%F`По умолчанию 0

`seaslog.remote_host`string

Якщо ви використовуєте запис TCP або UDP, налаштуйте віддалений IP. За промовчанням "127.0.0.1".

`seaslog.remote_port`int

Якщо ви використовуєте запис TCP або UDP, налаштуйте віддалений порт. Типово 514.

`seaslog.remote_timeout`int

Якщо ви використовуєте запис TCP або UDP, налаштуйте віддалений час очікування. За замовчуванням 1 секунда

`seaslog.throw_exception`int

Перемикає режим викиду виключення SeasLog. 1 - Так (за замовчуванням), 0 - Ні.

> **Зауваження** :
> 
> *seaslog.throw\_exception = 1* Відкриває виняток, який викидає сам SeasLog. Якщо адміністрація каталогу або порт приймаючого сервера заблоковано, викидається виняток; не викидається виняток під час закриття.

`seaslog.trace_error`int

Автоматичний запис "error" реєстратором за замовчуванням. 1 - Так (за замовчуванням), 0 - Ні.

`seaslog.trace_exception`int

Автоматичний запис "exception" реєстратор за замовчуванням. 1 - Так, 0 - Ні (за замовчуванням).

`seaslog.trace_notice`int

Автоматичний запис "notice" реєстратором за замовчуванням. 1 - Так, 0 - Ні (за замовчуванням).

`seaslog.trace_warning`int

Автоматичний запис "warning" реєстратором за замовчуванням. 1 - Так, 0 - Ні (за замовчуванням).

`seaslog.trim_wrap`int

Обрізає \\n и\\r у повідомленні журналу. 1 - Так, 0 - Ні (за замовчуванням)

`seaslog.use_buffer`int

Перемикає режим використання буфера журналу пам'яті. 1 - Так, 0 - Ні (за замовчуванням)

> **Зауваження** :
> 
> *seaslog.use\_buffer = 1*Включите configure use\_buffer. За замовчуванням use\_buffer вимкнено. Якщо увімкнути use\_buffer, SeasLog попередньо записуватиме журнал у пам'ять і він буде перезаписаний в сховище даних шляхом завершення запиту або виходу з процесу PHP (PHP RSHUTDOWN або PHP MSHUTDOWN).

`seaslog.default_template`string

Стандартний шаблон журналу. За замовчуванням "%T | %L | % P | % Q | % t | % M".

> **Зауваження** :
> 
> Надаються наступні змінні за замовчуванням, які можна використовувати безпосередньо у шаблоні журналу та замінювати відповідним значенням під час створення журналу.
> 
> Шаблон журнала по умолчанию:`seaslog.default_template = "%T | %L | %P | %Q | %t | %M"`, це означає, що стиль журналу за промовчанням: `{dateTime} | {level} | {pid} | {uniqid} | {timeStamp} | {logInfo}`
> 
> Якщо ви використовуєте власний шаблон журналу, наприклад: `seaslog.default_template = "[%T]:%L %P %Q %t %M"`, це означатиме, що стиль журналу був налаштований як: `[{dateTime}]:{level} {pid} {uniqid} {timeStamp} {logInfo}`
> 
> **Таблиця змінних за промовчанням Seaslog**
> 
> | Variable Name | Опис |
> | --- | --- |
> | %L | Рівень. |
> | %M | Повідомлення. |
> | %T | DateTime. Таке як `2017-08-16 19:15:02`, порушене `seaslog.default_datetime_format` |
> | %t | Timestamp. Таке як `1502882102.862`з точністю до мілісекунд. |
> | %Q | RequestId. Щоб розрізняти один запит, наприклад, не викликати функції `SeasLog::setRequestId($string)`При ініціалізації запиту використовується унікальне значення, згенероване вбудованою функцією. `static char *get_uniqid()` |
> | %H | HostName. |
> | %P | ProcessId. |
> | %D | Domain:Port. Таке як `www.cloudwise.com:80`; Якщо CLI, то `cli` |
> | %R | URI запиту. Такий як `/app/user/signin`; Якщо CLI, то, наприклад `CliIndex.php` |
> | %m | Спосіб запиту. Такий як `Get`; Якщо CLI, то використовується команда, наприклад, `/bin/bash` |
> | %I | IP-адреса клієнта; Якщо CLI, то `local`. . Пріоритет значень: HTTP\_X\_REAL\_IP > HTTP\_X\_FORWARDED\_FOR > REMOTE\_ADDR |
> | %F | FileName:LineNo. Таке як `UserService.php:118` |
> | %U | Замовленнявикористання в байтах. Виклик `zend_memory_usage` |
> | %u | PeakMemoryUsage в байтах. Виклик `zend_memory_peak_usage` |
> | %C | `TODO` Class::Action. Таке як `UserService::getUserInfo` |
