---
navigation:
  - seaslog.installation.md: « Установка
  - seaslog.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - seaslog.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Seaslog**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [seaslog.appender](seaslog.configuration.html#ini.seaslog.appender) |  | PHPINISYSTEM |  |
| [seaslog.appenderretry](seaslog.configuration.html#ini.seaslog.appender-retry) |  | PHPINIALL |  |
| [seaslog.level](seaslog.configuration.html#ini.seaslog.level) |  | PHPINIALL |  |
| [seaslog.remotehost](seaslog.configuration.html#ini.seaslog.remote-host) |  | PHPINIALL |  |
| [seaslog.remoteport](seaslog.configuration.html#ini.seaslog.remote-port) |  | PHPINIALL |  |
| [seaslog.remotetimeout](seaslog.configuration.html#ini.seaslog.remote-timeout) |  | PHPINISYSTEM |  |
| [seaslog.defaultbasepath](seaslog.configuration.html#ini.seaslog.default-basepath) | /var/log/www | PHPINISYSTEM |  |
| [seaslog.defaultlogger](seaslog.configuration.html#ini.seaslog.default-logger) | default | PHPINISYSTEM |  |
| [seaslog.defaulttemplate](seaslog.configuration.html#ini.seaslog.default-template) | %Т | %Л | %П |
| [seaslog.defaultdatetimeformat](seaslog.configuration.html#ini.seaslog.default-datetime-format) | Y-m-d H:i:s | PHPINISYSTEM |  |
| [seaslog.traceerror](seaslog.configuration.html#ini.seaslog.trace-error) |  | PHPINIALL |  |
| [seaslog.traceexception](seaslog.configuration.html#ini.seaslog.trace-exception) |  | PHPINISYSTEM |  |
| [seaslog.tracenotice](seaslog.configuration.html#ini.seaslog.trace-notice) |  | PHPINIALL |  |
| [seaslog.tracewarning](seaslog.configuration.html#ini.seaslog.trace-warning) |  | PHPINIALL |  |
| [seaslog.usebuffer](seaslog.configuration.html#ini.seaslog.use-buffer) |  | PHPINISYSTEM |  |
| [seaslog.buffersize](seaslog.configuration.html#ini.seaslog.buffer-size) |  | PHPINIALL |  |
| [seaslog.bufferdisabledінcli](seaslog.configuration.html#ini.seaslog.buffer-disabled-in-cli) |  | PHPINISYSTEM |  |
| [seaslog.distingtype](seaslog.configuration.html#ini.seaslog.disting-type) |  | PHPINISYSTEM |  |
| [seaslog.distingfolder](seaslog.configuration.html#ini.seaslog.disting-folder) |  | PHPINISYSTEM |  |
| [seaslog.distingбhour](seaslog.configuration.html#ini.seaslog.disting-by-hour) |  | PHPINISYSTEM |  |
| [seaslog.recalldepth](seaslog.configuration.html#ini.seaslog.recall-depth) |  | PHPINIALL |  |
| [seaslog.trimwrap](seaslog.configuration.html#ini.seaslog.trim-wrap) |  | PHPINIALL |  |
| [seaslog.ignorewarning](seaslog.configuration.html#ini.seaslog.ignore-warning) |  | PHPINIALL |  |
| [seaslog.throwexception](seaslog.configuration.html#ini.seaslog.throw-exception) |  | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`seaslog.appender` int

Перемикає сховище журналу записів. 1 – Файл, 2 – TCP, 3 – UDP (за замовчуванням 1)

SeasLog надішле журнал на сервер tcp://remotehost:remoteport або udp://remotehost:remoteport, якщо *seaslog.appender* налаштований на `2 (TCP)` або `3 (UDP)`

Коли *SeasLog* відправляє журнал TCP/UDP, стиль відповідає RFC5424 . `{logInfo}`, на який впливає *seaslog.defaulttemplate*

```
Стиль журнала отформатирован следующим образом:
<15>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | DEBUG | 21423 | 599157af4e937 | 1466787583.322 | this is a neeke debug
<14>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | INFO | 21423 | 599157af4e937 | 1466787583.323 | this is a info log
<13>1 2017-08-27T01:24:59+08:00 vagrant-ubuntu-trusty test/logger[27171]: 2016-06-25 00:59:43 | NOTICE | 21423 | 599157af4e937 | 1466787583.324 | this is a notice log
```

`seaslog.appender_retry` int

Записує кількість повторних спроб журналу. За замовчуванням 0 (не записує)

`seaslog.buffer_disabled_in_cli` int

Вимикає буфер у CLI. 1 - Так, 0 - Ні (за замовчуванням)

Увімкніть опцію bufferdisabledінклі. bufferdisabledінcli вимкнено за замовчуванням. Якщо увімкнути bufferdisabledінcli і запустити його в CLI, параметр seaslog.usebuffer буде скинутий, Seaslog НЕГАЙНО зробить запис у сховищі даних.

`seaslog.buffer_size` int

Вкажіть для параметра bufferзначення size 100. Значення bufferза замовчуванням 0, це означає, що буфер не використовується. Якщо buffersize > 0, SeasLog перезапише дані у сховищі, якщо розмір попередньо записаного в пам'ять журналу >= buffersize та оновіть опитування пам'яті.

`seaslog.default_basepath` string

Базовий шлях журналу за промовчанням. За промовчанням "/var/log/www".

`seaslog.default_datetime_format` string

Стиль DateTime. За промовчанням "Y-m-d H:i:s".

`seaslog.default_logger` string

Шлях до реєстратора за замовчуванням. За промовчанням "default".

`seaslog.disting_by_hour` int

Перемикає режим реєстратора щогодини. 1 - Так, 0 - Ні (за замовчуванням)

> **Зауваження**
> 
> *seaslog.distingбhour = 1* перемикає режим використання Logger DisTing щогодини. Це означає, що SeasLog буде створювати файл щогодини.

`seaslog.disting_folder` int

Перемикає режим використання реєстратора за папками. 1 - Так (за замовчуванням), 0 - Ні.

> **Зауваження**
> 
> *seaslog.distingfolder = 1* перемикає режим використання Logger DisTing за папками, це означає, що SeasLog буде створювати файли в папках і при цьому налаштуванні закриття SeasLog створить файл з підкресленням, використовуючи тип реєстратора та час, наприклад, default20180211.log.

`seaslog.disting_type` int

Перемикає режим використання реєстратора типу. 1 - Так, 0 - Ні (за замовчуванням)

> **Зауваження**
> 
> *seaslog.distingtype = 1* перемикає режим використання Logger DisTing за типом, це означає, що SeasLog створить файл infowarnerror чи іншого типу.

`seaslog.ignore_warning` int

Перемикає режим ігнорування попереджень SeasLog. 1 - Так (за замовчуванням), 0 - Ні.

> **Зауваження**
> 
> *seaslog.ignorewarning = 1* Відкриває попередження про ігнорування самого SeasLog. Коли права доступу до каталогу або порти сервера прийому заблоковані, вони ігноруються; під час закриття видається попередження.

`seaslog.level` int

Рівень запису реєстратора. Типово 8 (все). 0 - EMERGENCY, 1 - ALERT, 2 - CRITICAL, 3 - ERROR, 4 - WARNING, 5 - NOTICE, 6 - INFO, 7 - DEBUG, 8-ALL

> **Зауваження**
> 
> Примітка: елемент конфігурації змінено, починаючи з версії 1.7.0. До версії 1.7.0, чим менше значення, тим більше записів ведеться відповідно до рівня: 0 - все, 1 - debug, 2 - info, 3-notice, 4-warning, 5-error, 6-critical, 7-alert 8-емергенці. До версії 1.7.0 значення за промовчанням - 0 (все).

`seaslog.recall_depth` int

Глибина виклику функції журналу. Буде торкнутися змінної `LineNo` в `%F`. За замовчуванням 0

`seaslog.remote_host` string

Якщо ви використовуєте запис TCP або UDP, налаштуйте віддалений IP. За промовчанням "127.0.0.1".

`seaslog.remote_port` int

Якщо ви використовуєте запис TCP або UDP, налаштуйте віддалений порт. Типово 514.

`seaslog.remote_timeout` int

Якщо ви використовуєте запис TCP або UDP, налаштуйте віддалений час очікування. За замовчуванням 1 секунда

`seaslog.throw_exception` int

Перемикає режим викиду виключення SeasLog. 1 - Так (за замовчуванням), 0 - Ні.

> **Зауваження**
> 
> *seaslog.throwexception = 1* Відкриває виняток, який викидає сам SeasLog. Якщо адміністрація каталогу або порт приймаючого сервера заблоковано, викидається виняток; не викидається виняток під час закриття.

`seaslog.trace_error` int

Автоматичний запис "error" реєстратором за замовчуванням. 1 - Так (за замовчуванням), 0 - Ні.

`seaslog.trace_exception` int

Автоматичний запис "exception" реєстратор за замовчуванням. 1 - Так, 0 - Ні (за замовчуванням).

`seaslog.trace_notice` int

Автоматичний запис "notice" реєстратором за замовчуванням. 1 - Так, 0 - Ні (за замовчуванням).

`seaslog.trace_warning` int

Автоматичний запис "warning" реєстратором за замовчуванням. 1 - Так, 0 - Ні (за замовчуванням).

`seaslog.trim_wrap` int

Обрізає n та r у повідомленні журналу. 1 - Так, 0 - Ні (за замовчуванням)

`seaslog.use_buffer` int

Перемикає режим використання буфера журналу пам'яті. 1 - Так, 0 - Ні (за замовчуванням)

> **Зауваження**
> 
> *seaslog.usebuffer = 1* Увімкніть configure usebuffer. За замовчуванням usebuffer вимкнено. Якщо увімкнути usebuffer, SeasLog попередньо записуватиме журнал у пам'ять і він буде перезаписаний в сховище даних шляхом завершення запиту або виходу з процесу PHP (PHP RSHUTDOWN або PHP MSHUTDOWN).

`seaslog.default_template` string

Стандартний шаблон журналу. За замовчуванням "%T | %L | % P | % Q | % t | % M".

> **Зауваження**
> 
> Надаються такі змінні за замовчуванням, які можна використовувати безпосередньо у шаблоні журналу та замінювати відповідним значенням під час створення журналу.
> 
> Шаблон журналу за замовчуванням: `seaslog.default_template = "%T | %L | %P | %Q | %t | %M"`, це означає, що стиль журналу за промовчанням: `{dateTime} | {level} | {pid} | {uniqid} | {timeStamp} | {logInfo}`
> 
> Якщо ви використовуєте власний шаблон журналу, наприклад: `seaslog.default_template = "[%T]:%L %P %Q %t %M"`, це означатиме, що стиль журналу був налаштований як: `[{dateTime}]:{level} {pid} {uniqid} {timeStamp} {logInfo}`
> 
> **Таблиця змінних за промовчанням Seaslog**
> 
> | Variable Name | Описание |
> | --- | --- |
> | %Л | Рівень. |
> | %М | Повідомлення. |
> | %Т | DateTime. Таке як `2017-08-16 19:15:02`, порушене `seaslog.default_datetime_format` |
> | %т | Timestamp. Таке як `1502882102.862`з точністю до мілісекунд. |
> | %До | RequestId. Щоб розрізняти один запит, наприклад, не викликати функції `SeasLog::setRequestId($string)`, при ініціалізації запиту використовується унікальне значення, згенероване вбудованою функцією `static char *get_uniqid()` |
> | %Х | HostName. |
> | %П | ProcessId. |
> | %Д | Domain:Port. Таке як `www.cloudwise.com:80`; Якщо CLI, то `cli` |
> | %Р | URI запиту. Такий як `/app/user/signin`; Якщо CLI, то, наприклад `CliIndex.php` |
> | %м | Спосіб запиту. Такий як `Get`; Якщо CLI, то використовується команда, наприклад, `/bin/bash` |
> | %І | IP-адреса клієнта; Якщо CLI, то `local`. Пріоритет значень: HTTPЗREALIP > HTTPЗFORWARDEDFOR > REMOTEADDR |
> | %Ф | FileName:LineNo. Таке як `UserService.php:118` |
> | %У | Замовленнявикористання в байтах. Виклик `zend_memory_usage` |
> | %у | PeakMemoryUsage в байтах. Виклик `zend_memory_peak_usage` |
> | %С | `TODO` Class::Action. Таке як `UserService::getUserInfo` |
