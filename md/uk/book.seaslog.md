---
navigation:
  - class.random-randomexception.md: « Random\\RandomException
  - intro.seaslog.md: Вступ "
  - index.md: PHP Manual
  - refs.basic.other.md: Інші базові модулі
title: Seaslog
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Seaslog

-   [Вступ](intro.seaslog.md)
-   [Встановлення та налаштування](seaslog.setup.md)
    -   [Вимоги](seaslog.requirements.md)
    -   [Установка](seaslog.installation.md)
    -   [Налаштування під час виконання](seaslog.configuration.md)
    -   [Типи ресурсів](seaslog.resources.md)
-   [Обумовлені константи](seaslog.constants.md)
-   [Приклади](seaslog.examples.md)
-   [Функції Seaslog](ref.seaslog.md)
    -   [seaslog\_get\_author](function.seaslog-get-author.md)— Отримує автора SeasLog
    -   [seaslog\_get\_version](function.seaslog-get-version.md)— Отримує версію SeasLog
-   [SeasLog](class.seaslog.md) \- Клас SeasLog
    -   [SeasLog::alert](seaslog.alert.md) - Записує інформацію рівня "alert" у журнал
    -   [SeasLog::analyzerCount](seaslog.analyzercount.md)— Отримує кількість журналів за рівнем, log\_path і key\_word
    -   [SeasLog::analyzerDetail](seaslog.analyzerdetail.md)— Отримує деталізацію журналу за рівнем, log\_path, key\_word, start, limit, order
    -   [SeasLog::closeLoggerStream](seaslog.closeloggerstream.md) \- Вручну звільняє потік від реєстратора
    -   [SeasLog::\_\_construct](seaslog.construct.md) \- Опис
    -   [SeasLog::critical](seaslog.critical.md) - Записує інформацію рівня "critical" в журнал
    -   [SeasLog::debug](seaslog.debug.md) - Записує інформацію рівня "debug" в журнал
    -   [SeasLog::\_\_destruct](seaslog.destruct.md) \- Опис
    -   [SeasLog::emergency](seaslog.emergency.md) - Записує інформацію рівня "emergency" в журнал
    -   [SeasLog::error](seaslog.error.md) - Записує інформацію рівня "error" в журнал
    -   [SeasLog::flushBuffer](seaslog.flushbuffer.md)— Очищає буфер логів, робить дамп у файл програми або відправляє на віддалений API за допомогою tcp/udp
    -   [SeasLog::getBasePath](seaslog.getbasepath.md)— Отримує базовий шлях SeasLog
    -   [SeasLog::getBuffer](seaslog.getbuffer.md)— Отримує буфер логів у пам'яті у вигляді масиву
    -   [SeasLog::getBufferEnabled](seaslog.getbufferenabled.md)— Визначає, чи увімкнено буфер
    -   [SeasLog::getDatetimeFormat](seaslog.getdatetimeformat.md)— Отримує стиль формату дати та часу SeasLog
    -   [SeasLog::getLastLogger](seaslog.getlastlogger.md)— Отримує останній шлях реєстратора SeasLog
    -   [SeasLog::getRequestID](seaslog.getrequestid.md)— Отримує диференційовані запити SeasLog request\_id
    -   [SeasLog::getRequestVariable](seaslog.getrequestvariable.md)— Отримує змінну запиту SeasLog
    -   [SeasLog::info](seaslog.info.md) - Записує інформацію рівня "info" в журнал
    -   [SeasLog::log](seaslog.log.md)— Загальна функція запису до журналу
    -   [SeasLog::notice](seaslog.notice.md) - Записує інформацію рівня "notice" в журнал
    -   [SeasLog::setBasePath](seaslog.setbasepath.md) \- Встановлює базовий шлях SeasLog
    -   [SeasLog::setDatetimeFormat](seaslog.setdatetimeformat.md)— Встановлює стиль формату дати та часу SeasLog
    -   [SeasLog::setLogger](seaslog.setlogger.md) \- Встановлює ім'я реєстратора SeasLog
    -   [SeasLog::setRequestID](seaslog.setrequestid.md)— Встановлює диференційовані запити SeasLog request\_id
    -   [SeasLog::setRequestVariable](seaslog.setrequestvariable.md)— Встановлює змінну запиту SeasLog вручну
    -   [SeasLog::warning](seaslog.warning.md) - Записує інформацію рівня "warning" в журнал
