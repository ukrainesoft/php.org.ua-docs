Обумовлені константи

-   [« Типы ресурсов](seaslog.resources.html)
    
-   [Примеры »](seaslog.examples.html)
    
-   [PHP Manual](index.html)
    
-   [Seaslog](book.seaslog.html)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

**`SEASLOG_VERSION`** (string)

**`SEASLOG_AUTHOR`** (string)

**`SEASLOG_ALL`** (string)

"ALL"

**`SEASLOG_DEBUG`** (string)

"DEBUG" - Детальна інформація про налагодження. Детальні інформаційні події.

**`SEASLOG_INFO`** (string)

"INFO" - інформаційні події. Підкреслює запущений процес застосування.

**`SEASLOG_NOTICE`** (string)

"NOTICE" - нормальні, але важливі події. Інформація, яка важливіша за рівень INFO під час виконання.

**`SEASLOG_WARNING`** (string)

"WARNING" - Виняткові випадки, які є помилками. Потенційно помилкова інформація, яка потребує уваги та потребує виправлення.

**`SEASLOG_ERROR`** (string)

"ERROR" - Помилки під час виконання, які не вимагають негайних дій, але зазвичай мають бути виправлені.

**`SEASLOG_CRITICAL`** (string)

"CRITICAL" - Критичні умови. Потрібне негайне виправлення, програмний компонент недоступний.

**`SEASLOG_ALERT`** (string)

"ALERT" - Дії мають бути здійснені негайно. Негайну увагу слід приділити відповідному персоналу для аварійного ремонту.

**`SEASLOG_EMERGENCY`** (string)

"EMERGENCY" - Система непридатна для використання.

**`SEASLOG_DETAIL_ORDER_ASC`** (int)

**`SEASLOG_DETAIL_ORDER_DESC`** (int)

**`SEASLOG_APPENDER_FILE`** (int)

**`SEASLOG_APPENDER_TCP`** (int)

**`SEASLOG_APPENDER_UDP`** (int)

**`SEASLOG_CLOSE_LOGGER_STREAM_MOD_ALL`** (int)

**`SEASLOG_CLOSE_LOGGER_STREAM_MOD_ASSIGN`** (int)

**`SEASLOG_REQUEST_VARIABLE_DOMAIN_PORT`** (int)

**`SEASLOG_REQUEST_VARIABLE_REQUEST_URI`** (int)

**`SEASLOG_REQUEST_VARIABLE_REQUEST_METHOD`** (int)

**`SEASLOG_REQUEST_VARIABLE_CLIENT_IP`** (int)