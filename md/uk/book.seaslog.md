Seaslog

-   [« Список изменений](changelog.misc.html)
    
-   [Введение »](intro.seaslog.html)
    
-   [PHP Manual](index.html)
    
-   [Другие базовые модули](refs.basic.other.html)
    
-   Seaslog
    

# Seaslog

-   [Введение](intro.seaslog.html)
-   [Установка и настройка](seaslog.setup.html)
    -   [Требования](seaslog.requirements.html)
    -   [Установка](seaslog.installation.html)
    -   [Настройка во время выполнения](seaslog.configuration.html)
    -   [Типы ресурсов](seaslog.resources.html)
-   [Предопределённые константы](seaslog.constants.html)
-   [Примеры](seaslog.examples.html)
-   [Функции Seaslog](ref.seaslog.html)
    -   [seaslog\_get\_author](function.seaslog-get-author.html) — Отримує автора SeasLog
    -   [seaslog\_get\_version](function.seaslog-get-version.html) — Отримує версію SeasLog
-   [SeasLog](class.seaslog.html) - Клас SeasLog
    -   [SeasLog::alert](seaslog.alert.html) - Записує інформацію рівня "alert" у журнал
    -   [SeasLog::analyzerCount](seaslog.analyzercount.html) — Отримує кількість журналів за рівнем, logpath і keyслово
    -   [SeasLog::analyzerDetail](seaslog.analyzerdetail.html) — Отримує деталізацію журналу за рівнем, logpath, keyword, start, limit, order
    -   [SeasLog::closeLoggerStream](seaslog.closeloggerstream.html) - Вручну звільняє потік від реєстратора
    -   [SeasLog::\_\_construct](seaslog.construct.html) - Опис
    -   [SeasLog::critical](seaslog.critical.html) - Записує інформацію рівня "critical" в журнал
    -   [SeasLog::debug](seaslog.debug.html) - Записує інформацію рівня "debug" в журнал
    -   [SeasLog::\_\_destruct](seaslog.destruct.html) - Опис
    -   [SeasLog::emergency](seaslog.emergency.html) - Записує інформацію рівня "emergency" в журнал
    -   [SeasLog::error](seaslog.error.html) - Записує інформацію рівня "error" в журнал
    -   [SeasLog::flushBuffer](seaslog.flushbuffer.html) — Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
    -   [SeasLog::getBasePath](seaslog.getbasepath.html) — Отримує базовий шлях SeasLog
    -   [SeasLog::getBuffer](seaslog.getbuffer.html) — Отримує буфер логів у пам'яті у вигляді масиву
    -   [SeasLog::getBufferEnabled](seaslog.getbufferenabled.html) — Визначає, чи увімкнено буфер
    -   [SeasLog::getDatetimeFormat](seaslog.getdatetimeformat.html) — Отримує стиль формату дати та часу SeasLog
    -   [SeasLog::getLastLogger](seaslog.getlastlogger.html) — Отримує останній шлях реєстратора SeasLog
    -   [SeasLog::getRequestID](seaslog.getrequestid.html) — Отримує диференційовані запити SeasLog requestід
    -   [SeasLog::getRequestVariable](seaslog.getrequestvariable.html) — Отримує змінну запиту SeasLog
    -   [SeasLog::info](seaslog.info.html) - Записує інформацію рівня "info" в журнал
    -   [SeasLog::log](seaslog.log.html) — Загальна функція запису до журналу
    -   [SeasLog::notice](seaslog.notice.html) - Записує інформацію рівня "notice" в журнал
    -   [SeasLog::setBasePath](seaslog.setbasepath.html) - Встановлює базовий шлях SeasLog
    -   [SeasLog::setDatetimeFormat](seaslog.setdatetimeformat.html) — Встановлює стиль формату дати та часу SeasLog
    -   [SeasLog::setLogger](seaslog.setlogger.html) - Встановлює ім'я реєстратора SeasLog
    -   [SeasLog::setRequestID](seaslog.setrequestid.html) — Встановлює диференційовані запити SeasLog requestід
    -   [SeasLog::setRequestVariable](seaslog.setrequestvariable.html) — Встановлює змінну запиту SeasLog вручну
    -   [SeasLog::warning](seaslog.warning.html) - Записує інформацію рівня "warning" в журнал