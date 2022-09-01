---
navigation:
  - function.seaslog-get-version.html: « seasloggetversion
  - seaslog.alert.md: 'SeasLog::alert »'
  - index.md: PHP Manual
  - book.seaslog.md: Seaslog
title: Клас SeasLog
---
# Клас SeasLog

(PECL seaslog >=1.0.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class SeasLog
     
     {


    /* Методы */
    
   public static alert(string $message, array $content = ?, string $logger = ?): bool
public static analyzerCount(string $level, string $log_path = ?, string $key_word = ?): mixed
public static analyzerDetail(    string $level,    string $log_path = ?,    string $key_word = ?,    int $start = ?,    int $limit = ?,    int $order = ?): mixed
public static closeLoggerStream(int $model, string $logger): bool
public static critical(string $message, array $content = ?, string $logger = ?): bool
public static debug(string $message, array $content = ?, string $logger = ?): bool
public __destruct()
public static emergency(string $message, array $content = ?, string $logger = ?): bool
public static error(string $message, array $content = ?, string $logger = ?): bool
public static flushBuffer(): bool
public static Seaslog::getBasePath(): string
public static getBuffer(): array
public static getBufferEnabled(): bool
public static getDatetimeFormat(): string
public static getLastLogger(): string
public static getRequestID(): string
public static getRequestVariable(int $key): bool
public static info(string $message, array $content = ?, string $logger = ?): bool
public static log(    string $level,    string $message = ?,    array $content = ?,    string $logger = ?): bool
public static notice(string $message, array $content = ?, string $logger = ?): bool
public static setBasePath(string $base_path): bool
public static setDatetimeFormat(string $format): bool
public static setLogger(string $logger): bool
public static setRequestID(string $request_id): bool
public static setRequestVariable(int $key, string $value): bool
public static warning(string $message, array $content = ?, string $logger = ?): bool

   }
```

## Зміст

-   [SeasLog::alert](seaslog.alert.md) - Записує інформацію рівня "alert" у журнал
-   [SeasLog::analyzerCount](seaslog.analyzercount.md) — Отримує кількість журналів за рівнем, logpath і keyслово
-   [SeasLog::analyzerDetail](seaslog.analyzerdetail.md) — Отримує деталізацію журналу за рівнем, logpath, keyword, start, limit, order
-   [SeasLog::closeLoggerStream](seaslog.closeloggerstream.md) - Вручну звільняє потік від реєстратора
-   [SeasLog::construct](seaslog.construct.md) - Опис
-   [SeasLog::critical](seaslog.critical.md) - Записує інформацію рівня "critical" в журнал
-   [SeasLog::debug](seaslog.debug.md) - Записує інформацію рівня "debug" в журнал
-   [SeasLog::destruct](seaslog.destruct.md) - Опис
-   [SeasLog::emergency](seaslog.emergency.md) - Записує інформацію рівня "emergency" в журнал
-   [SeasLog::error](seaslog.error.md) - Записує інформацію рівня "error" в журнал
-   [SeasLog::flushBuffer](seaslog.flushbuffer.md) — Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
-   [SeasLog::getBasePath](seaslog.getbasepath.md) — Отримує базовий шлях SeasLog
-   [SeasLog::getBuffer](seaslog.getbuffer.md) — Отримує буфер логів у пам'яті у вигляді масиву
-   [SeasLog::getBufferEnabled](seaslog.getbufferenabled.md) — Визначає, чи увімкнено буфер
-   [SeasLog::getDatetimeFormat](seaslog.getdatetimeformat.md) — Отримує стиль формату дати та часу SeasLog
-   [SeasLog::getLastLogger](seaslog.getlastlogger.md) — Отримує останній шлях реєстратора SeasLog
-   [SeasLog::getRequestID](seaslog.getrequestid.md) — Отримує диференційовані запити SeasLog requestід
-   [SeasLog::getRequestVariable](seaslog.getrequestvariable.md) — Отримує змінну запиту SeasLog
-   [SeasLog::info](seaslog.info.md) - Записує інформацію рівня "info" в журнал
-   [SeasLog::log](seaslog.log.md) — Загальна функція запису до журналу
-   [SeasLog::notice](seaslog.notice.md) - Записує інформацію рівня "notice" в журнал
-   [SeasLog::setBasePath](seaslog.setbasepath.md) - Встановлює базовий шлях SeasLog
-   [SeasLog::setDatetimeFormat](seaslog.setdatetimeformat.md) — Встановлює стиль формату дати та часу SeasLog
-   [SeasLog::setLogger](seaslog.setlogger.md) - Встановлює ім'я реєстратора SeasLog
-   [SeasLog::setRequestID](seaslog.setrequestid.md) — Встановлює диференційовані запити SeasLog requestід
-   [SeasLog::setRequestVariable](seaslog.setrequestvariable.md) — Встановлює змінну запиту SeasLog вручну
-   [SeasLog::warning](seaslog.warning.md) - Записує інформацію рівня "warning" в журнал
