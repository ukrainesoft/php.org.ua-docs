- [« SeasLog::log](seaslog.log.md)
- [SeasLog::setBasePath »](seaslog.setbasepath.md)

- [PHP Manual](index.md)
- [SeasLog](class.seaslog.md)
- Записує інформацію рівня "notice" у журнал

# SeasLog::notice

(PECL seaslog \>=1.0.0)

SeasLog::notice — Записує інформацію рівня "notice" у журнал

### Опис

public static **SeasLog::notice**(string `$message`, array `$content` =
?, string `$logger` = ?): bool

Записує інформацію рівня "notice" у журнал.

> **Примітка**:
>
> "NOTICE" - нормальні, але важливі події. Інформація, яка важливіша
> рівня "info" під час виконання.

### Список параметрів

`message`
Повідомлення журналу.

`content`
Повідомлення містить наповнювачі, які розробники замінюють значеннями
із масиву вмісту. Якщо "message" - це інформація журналу від
{NAME}\`, а \`content\` - \`array('NAME' =\> 'Нікіти')\`, інформація
журналу буде "інформація журналу від Микити".

`logger`
\`logger\`, укладений у третій параметр, використовуватиметься прямо
зараз, як тимчасовий реєстратор, якщо функція SeasLog::setLogger()
викликається у попередньому вмісті. Якщо logger дорівнює NULL або
"" (порожній рядок), SeasLog буде використовувати останній реєстратор,
встановлений методом [SeasLog::setLogger()](seaslog.setlogger.md).

### Значення, що повертаються

Повертає TRUE у разі успішного виконання запису журналу, FALSE в
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SeasLog::notice()****

` <?phpvar_dump(SeasLog::notice('log message'));//с contentvar_dump(SeasLog::notice('log message from {NAME}',array('NAME' => 'neeke'))); //з часовим loggervar_dump(SeasLog::notice('log message from {NAME}',array('NAME' => 'neeke'),'tmp_logger'));var_dump(SeasLog::getBuffer());?> `

Результатом виконання цього прикладу буде щось подібне:

bool(true)
bool(true)
bool(true)
array(2) {
["/var/log/www/default/20180707.log"]=>
array(2) {
[0]=>
string(81) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message
"
[1]=>
string(92) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
}
["/var/log/www/tmp_logger/20180707.log"]=>
array(1) {
[0]=>
string(92) "2018-07-07 11:45:49 | NOTICE | 73263 | 5b40376d1067c | 1530935149.68 | log message from neeke
"
}
}

### Дивіться також

- [seaslog.default_template](seaslog.configuration.md#ini.seaslog.default-template)
- [SeasLog::debug()](seaslog.debug.md) - Записує інформацію
рівня "debug" до журналу
- [SeasLog::info()](seaslog.info.md) - Записує інформацію рівня
"info" у журнал
- [SeasLog::warning()](seaslog.warning.md) - Записує інформацію
рівня "warning" до журналу
- [SeasLog::error()](seaslog.error.md) - Записує інформацію
рівня "error" у журнал
- [SeasLog::critical()](seaslog.critical.md) - Записує інформацію
рівня "critical" у журнал
- [SeasLog::alert()](seaslog.alert.md) - Записує інформацію
рівня "alert" у журнал
- [SeasLog::emergency()](seaslog.emergency.md) - Записує
інформацію рівня "emergency" до журналу
- [SeasLog::log()](seaslog.log.md) - Загальна функція запису в журнал
