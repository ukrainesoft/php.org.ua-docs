Клас mysqli

-   [« Основная информация о функциях модуля MySQLi](mysqli.summary.html)
    
-   [mysqli::$affected\_rows »](mysqli.affected-rows.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   Клас mysqli
    

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

-   [mysqli::$affected\_rows](mysqli.affected-rows.html) — Отримує кількість рядків, які торкнулися попередньої операції MySQL
-   [mysqli::autocommit](mysqli.autocommit.html) — Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqli::begin\_transaction](mysqli.begin-transaction.html) - Стартує транзакцію
-   [mysqli::change\_user](mysqli.change-user.html) — Дозволяє змінити користувача підключеного до бази даних
-   [mysqli::character\_set\_name](mysqli.character-set-name.html) — Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqli::close](mysqli.close.html) — Закриває раніше відкрите з'єднання з базою даних
-   [mysqli::commit](mysqli.commit.html) - Фіксує поточну транзакцію
-   [mysqli::$connect\_errno](mysqli.connect-errno.html) — Повертає код помилки останньої спроби з'єднання
-   [mysqli::$connect\_error](mysqli.connect-error.html) — Повертає опис останньої помилки підключення
-   [mysqli::\_\_construct](mysqli.construct.html) — Встановлює нове з'єднання із сервером MySQL
-   [mysqli::debug](mysqli.debug.html) - Виконує процедури налагодження
-   [mysqli::dump\_debug\_info](mysqli.dump-debug-info.html) - Журналування налагоджувальної інформації
-   [mysqli::$errno](mysqli.errno.html) — Повертає код помилки останнього виклику функції
-   [mysqli::$error\_list](mysqli.error-list.html) — Повертає перелік помилок виконання останньої запущеної команди
-   [mysqli::$error](mysqli.error.html) — Повертає рядок із описом останньої помилки
-   [mysqli::$field\_count](mysqli.field-count.html) — Повертає кількість стовпців, які торкнулися останнім запитом
-   [mysqli::get\_charset](mysqli.get-charset.html) — Повертає об'єкт, що описує кодування
-   [mysqli::$client\_info](mysqli.get-client-info.html) — Отримує інформацію про клієнта MySQL
-   [mysqli::$client\_version](mysqli.get-client-version.html) — Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli::get\_connection\_stats](mysqli.get-connection-stats.html) — Повертає статистику з'єднання із клієнтом
-   [mysqli::$host\_info](mysqli.get-host-info.html) — Повертає рядок, що містить тип використовуваної сполуки
-   [mysqli::$protocol\_version](mysqli.get-proto-info.html) — Повертає версію протоколу, що використовується MySQL
-   [mysqli::$server\_info](mysqli.get-server-info.html) — Повертає версію сервера MySQL
-   [mysqli::$server\_version](mysqli.get-server-version.html) — Повертає версію сервера MySQL, представлену у вигляді integer
-   [mysqli::get\_warnings](mysqli.get-warnings.html) — Отримує результат SHOW WARNINGS
-   [mysqli::$info](mysqli.info.html) — Витягує інформацію про останній запит
-   [mysqli::init](mysqli.init.html) — Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqlirealconnect()
-   [mysqli::$insert\_id](mysqli.insert-id.html) — Повертає значення, створене для стовпця AUTOINCREMENT останнім запитом
-   [mysqli::kill](mysqli.kill.html) — Запит для сервера завершити виконання процесу MySQL
-   [mysqli::more\_results](mysqli.more-results.html) — Перевірка, чи є ще результати у мультизапиті
-   [mysqli::multi\_query](mysqli.multi-query.html) — Виконує один або кілька запитів до бази даних
-   [mysqli::next\_result](mysqli.next-result.html) — Підготовка наступного результуючого набору з multiquery
-   [mysqli::options](mysqli.options.html) — Встановлення налаштувань
-   [mysqli::ping](mysqli.ping.html) — Перевіряє працездатність з'єднання або намагається перепідключитися, якщо з'єднання розірвано
-   [mysqli::poll](mysqli.poll.html) - Опитування підключень
-   [mysqli::prepare](mysqli.prepare.html) - Підготовляє SQL вираз до виконання
-   [mysqli::query](mysqli.query.html) — Виконує запит до бази даних
-   [mysqli::real\_connect](mysqli.real-connect.html) — Встановлює з'єднання із сервером mysql
-   [mysqli::real\_escape\_string](mysqli.real-escape-string.html) — Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
-   [mysqli::real\_query](mysqli.real-query.html) - Виконання SQL запиту
-   [mysqli::reap\_async\_query](mysqli.reap-async-query.html) — Отримання результату асинхронного запиту
-   [mysqli::refresh](mysqli.refresh.html) - Оновлення
-   [mysqli::release\_savepoint](mysqli.release-savepoint.html) — Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції.
-   [mysqli::rollback](mysqli.rollback.html) - Відкат поточної транзакції
-   [mysqli::savepoint](mysqli.savepoint.html) — Встановіть іменовану точку збереження транзакції
-   [mysqli::select\_db](mysqli.select-db.html) — Встановлює базу даних для запитів, що виконуються.
-   [mysqli::set\_charset](mysqli.set-charset.html) — Задає набір символів
-   [mysqli::$sqlstate](mysqli.sqlstate.html) — Повертає код стану SQLSTATE останньої операції MySQL операції
-   [mysqli::ssl\_set](mysqli.ssl-set.html) — Використовується для встановлення безпечних з'єднань за допомогою SSL
-   [mysqli::stat](mysqli.stat.html) - Отримання інформації про поточний стан системи
-   [mysqli::stmt\_init](mysqli.stmt-init.html) — Ініціалізує запит та повертає об'єкт для використання у mysqlistmtprepare
-   [mysqli::store\_result](mysqli.store-result.html) — передає на клієнта результуючий набір останнього запиту
-   [mysqli::$thread\_id](mysqli.thread-id.html) — Повертає ID процесу поточного підключення
-   [mysqli::thread\_safe](mysqli.thread-safe.html) — Показує, чи безпечна робота із процесами
-   [mysqli::use\_result](mysqli.use-result.html) — Готує результуючий набір на сервері для використання
-   [mysqli::$warning\_count](mysqli.warning-count.html) — Повертає кількість попереджень із останнього запиту заданого підключення