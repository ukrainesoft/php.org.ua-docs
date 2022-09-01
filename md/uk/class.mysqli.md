---
navigation:
  - mysqli.summary.md: « Основна інформація про функції модуля MySQLi
  - mysqli.affected-rows.html: 'mysqli::$affectedrows »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqli
---
# Клас mysqli

(PHP 5, PHP 7, PHP 8)

## Вступ

Представляє зв'язок між PHP та базою даних MySQL.

## Огляд класів

```classsynopsis

     
    

    
     
      class mysqli
     
     {

    /* Свойства */
    
     public
     readonly
     int|string
      $affected_rows;

    public
     readonly
     string
      $client_info;

    public
     readonly
     int
      $client_version;

    public
     readonly
     int
      $connect_errno;

    public
     readonly
     ?string
      $connect_error;

    public
     readonly
     int
      $errno;

    public
     readonly
     string
      $error;

    public
     readonly
     array
      $error_list;

    public
     readonly
     int
      $field_count;

    public
     readonly
     string
      $host_info;

    public
     readonly
     ?string
      $info;

    public
     readonly
     int|string
      $insert_id;

    public
     readonly
     string
      $server_info;

    public
     readonly
     int
      $server_version;

    public
     readonly
     string
      $sqlstate;

    public
     readonly
     int
      $protocol_version;

    public
     readonly
     int
      $thread_id;

    public
     readonly
     int
      $warning_count;


    /* Методы */
    
   public __construct(    string $hostname = ini_get("mysqli.default_host"),    string $username = ini_get("mysqli.default_user"),    string $password = ini_get("mysqli.default_pw"),    string $database = "",    int $port = ini_get("mysqli.default_port"),    string $socket = ini_get("mysqli.default_socket"))

    public autocommit(bool $enable): bool
public begin_transaction(int $flags = 0, ?string $name = null): bool
public change_user(string $username, string $password, ?string $database): bool
public character_set_name(): string
public close(): bool
public commit(int $flags = 0, ?string $name = null): bool
public connect(    string $hostname = ini_get("mysqli.default_host"),    string $username = ini_get("mysqli.default_user"),    string $password = ini_get("mysqli.default_pw"),    string $database = "",    int $port = ini_get("mysqli.default_port"),    string $socket = ini_get("mysqli.default_socket")): void
public debug(string $options): bool
public dump_debug_info(): bool
public get_charset(): ?object
public get_client_info(): string
public get_connection_stats(): array
public mysqli_stmt::get_server_info(): string
public get_warnings(): mysqli_warning|false
public kill(int $process_id): bool
public more_results(): bool
public multi_query(string $query): bool
public next_result(): bool
public options(int $option, string|int $value): bool
public ping(): bool
public static poll(    ?array &$read,    ?array &$error,    array &$reject,    int $seconds,    int $microseconds = 0): int|false
public prepare(string $query): mysqli_stmt|false
public query(string $query, int $result_mode = MYSQLI_STORE_RESULT): mysqli_result|bool
public real_connect(    string $host = ?,    string $username = ?,    string $passwd = ?,    string $dbname = ?,    int $port = ?,    string $socket = ?,    int $flags = ?): bool
public real_escape_string(string $string): string
public real_query(string $query): bool
public reap_async_query(): mysqli_result|bool
public refresh(int $flags): bool
public release_savepoint(string $name): bool
public rollback(int $flags = 0, ?string $name = null): bool
public savepoint(string $name): bool
public select_db(string $database): bool
public set_charset(string $charset): bool
public ssl_set(    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): bool
public stat(): string|false
public stmt_init(): mysqli_stmt|false
public store_result(int $mode = 0): mysqli_result|false
public thread_safe(): bool
public use_result(): mysqli_result|false

   }
```

## Зміст

-   [mysqli::$affectedrows](mysqli.affected-rows.md) — Отримує кількість рядків, які торкнулися попередньої операції MySQL
-   [mysqli::autocommit](mysqli.autocommit.md) — Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqli::begintransaction](mysqli.begin-transaction.md) - Стартує транзакцію
-   [mysqli::changeuser](mysqli.change-user.md) — Дозволяє змінити користувача підключеного до бази даних
-   [mysqli::charactersetname](mysqli.character-set-name.md) — Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqli::close](mysqli.close.md) — Закриває раніше відкрите з'єднання з базою даних
-   [mysqli::commit](mysqli.commit.md) - Фіксує поточну транзакцію
-   [mysqli::$connecterrno](mysqli.connect-errno.md) — Повертає код помилки останньої спроби з'єднання
-   [mysqli::$connecterror](mysqli.connect-error.md) — Повертає опис останньої помилки підключення
-   [mysqli::construct](mysqli.construct.md) — Встановлює нове з'єднання із сервером MySQL
-   [mysqli::debug](mysqli.debug.md) - Виконує процедури налагодження
-   [mysqli::dumpdebuginfo](mysqli.dump-debug-info.md) - Журналування налагоджувальної інформації
-   [mysqli::$errno](mysqli.errno.md) — Повертає код помилки останнього виклику функції
-   [mysqli::$errorlist](mysqli.error-list.md) — Повертає перелік помилок виконання останньої запущеної команди
-   [mysqli::$error](mysqli.error.md) — Повертає рядок із описом останньої помилки
-   [mysqli::$fieldcount](mysqli.field-count.md) — Повертає кількість стовпців, які торкнулися останнім запитом
-   [mysqli::getcharset](mysqli.get-charset.md) — Повертає об'єкт, що описує кодування
-   [mysqli::$clientinfo](mysqli.get-client-info.md) — Отримує інформацію про клієнта MySQL
-   [mysqli::$clientversion](mysqli.get-client-version.md) — Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli::getconnectionstats](mysqli.get-connection-stats.md) — Повертає статистику з'єднання із клієнтом
-   [mysqli::$hostinfo](mysqli.get-host-info.md) — Повертає рядок, що містить тип використовуваної сполуки
-   [mysqli::$protocolversion](mysqli.get-proto-info.md) — Повертає версію протоколу, що використовується MySQL
-   [mysqli::$serverinfo](mysqli.get-server-info.md) — Повертає версію сервера MySQL
-   [mysqli::$serverversion](mysqli.get-server-version.md) — Повертає версію сервера MySQL, представлену у вигляді integer
-   [mysqli::getwarnings](mysqli.get-warnings.md) — Отримує результат SHOW WARNINGS
-   [mysqli::$info](mysqli.info.md) — Витягує інформацію про останній запит
-   [mysqli::init](mysqli.init.md) — Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
-   [mysqli::$insertід](mysqli.insert-id.md) — Повертає значення, створене для стовпця AUTOINCREMENT останнім запитом
-   [mysqli::kill](mysqli.kill.md) — Запит для сервера завершити виконання процесу MySQL
-   [mysqli::moreresults](mysqli.more-results.md) — Перевірка, чи є ще результати у мультизапиті
-   [mysqli::multiquery](mysqli.multi-query.md) — Виконує один або кілька запитів до бази даних
-   [mysqli::nextresult](mysqli.next-result.md) — Підготовка наступного результуючого набору з multiquery
-   [mysqli::options](mysqli.options.md) — Встановлення налаштувань
-   [mysqli::ping](mysqli.ping.md) — Перевіряє працездатність з'єднання або намагається перепідключитися, якщо з'єднання розірвано
-   [mysqli::poll](mysqli.poll.md) - Опитування підключень
-   [mysqli::prepare](mysqli.prepare.md) - Підготовляє SQL вираз до виконання
-   [mysqli::query](mysqli.query.md) — Виконує запит до бази даних
-   [mysqli::realconnect](mysqli.real-connect.md) — Встановлює з'єднання із сервером mysql
-   [mysqli::realescapestring](mysqli.real-escape-string.md) — Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
-   [mysqli::realquery](mysqli.real-query.md) - Виконання SQL запиту
-   [mysqli::reapasyncquery](mysqli.reap-async-query.md) — Отримання результату асинхронного запиту
-   [mysqli::refresh](mysqli.refresh.md) - Оновлення
-   [mysqli::releasesavepoint](mysqli.release-savepoint.md) — Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції.
-   [mysqli::rollback](mysqli.rollback.md) - Відкат поточної транзакції
-   [mysqli::savepoint](mysqli.savepoint.md) — Встановіть іменовану точку збереження транзакції
-   [mysqli::selectдб](mysqli.select-db.md) — Встановлює базу даних для запитів, що виконуються.
-   [mysqli::setcharset](mysqli.set-charset.md) — Задає набір символів
-   [mysqli::$sqlstate](mysqli.sqlstate.md) — Повертає код стану SQLSTATE останньої операції MySQL операції
-   [mysqli::sslset](mysqli.ssl-set.md) — Використовується для встановлення безпечних з'єднань за допомогою SSL
-   [mysqli::stat](mysqli.stat.md) - Отримання інформації про поточний стан системи
-   [mysqli::stmtinit](mysqli.stmt-init.md) — Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare
-   [mysqli::storeresult](mysqli.store-result.md) — передає на клієнта результуючий набір останнього запиту
-   [mysqli::$threadід](mysqli.thread-id.md) — Повертає ID процесу поточного підключення
-   [mysqli::threadsafe](mysqli.thread-safe.md) — Показує, чи безпечна робота із процесами
-   [mysqli::useresult](mysqli.use-result.md) — Готує результуючий набір на сервері для використання
-   [mysqli::$warningcount](mysqli.warning-count.md) — Повертає кількість попереджень із останнього запиту заданого підключення
