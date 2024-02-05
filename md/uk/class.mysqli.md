---
navigation:
  - mysqli.summary.md: « Основна інформація про функції модуля MySQLi
  - mysqli.affected-rows.md: 'mysqli::$affected\_rows »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqli
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
    
   public __construct(    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null)

    public autocommit(bool $enable): bool
public begin_transaction(int $flags = 0, ?string $name = null): bool
public change_user(string $username, string $password, ?string $database): bool
public character_set_name(): string
public close(): true
public commit(int $flags = 0, ?string $name = null): bool
public connect(    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null): bool
public debug(string $options): true
public dump_debug_info(): bool
public execute_query(string $query, ?array $params = null): mysqli_result|bool
public get_charset(): ?object
public get_client_info(): string
public get_connection_stats(): array
public mysqli_stmt::get_server_info(): string
public get_warnings(): mysqli_warning|false
public init(): ?bool
public kill(int $process_id): bool
public more_results(): bool
public multi_query(string $query): bool
public next_result(): bool
public options(int $option, string|int $value): bool
public ping(): bool
public static poll(    ?array &$read,    ?array &$error,    array &$reject,    int $seconds,    int $microseconds = 0): int|false
public prepare(string $query): mysqli_stmt|false
public query(string $query, int $result_mode = MYSQLI_STORE_RESULT): mysqli_result|bool
public real_connect(    ?string $hostname = null,    ?string $username = null,    ?string $password = null,    ?string $database = null,    ?int $port = null,    ?string $socket = null,    int $flags = 0): bool
public real_escape_string(string $string): string
public real_query(string $query): bool
public reap_async_query(): mysqli_result|bool
public refresh(int $flags): bool
public release_savepoint(string $name): bool
public rollback(int $flags = 0, ?string $name = null): bool
public savepoint(string $name): bool
public select_db(string $database): bool
public set_charset(string $charset): bool
public ssl_set(    ?string $key,    ?string $certificate,    ?string $ca_certificate,    ?string $ca_path,    ?string $cipher_algos): true
public stat(): string|false
public stmt_init(): mysqli_stmt|false
public store_result(int $mode = 0): mysqli_result|false
public thread_safe(): bool
public use_result(): mysqli_result|false

   }
```

## Зміст

-   [mysqli::$affected\_rows](mysqli.affected-rows.md)— Отримує кількість рядків, які торкнулися попередньої операції MySQL
-   [mysqli::autocommit](mysqli.autocommit.md)— Вмикає або вимикає автоматичну фіксацію змін бази даних
-   [mysqli::begin\_transaction](mysqli.begin-transaction.md) \- Стартує транзакцію
-   [mysqli::change\_user](mysqli.change-user.md)— Дозволяє змінити користувача підключеного до бази даних
-   [mysqli::character\_set\_name](mysqli.character-set-name.md)— Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqli::close](mysqli.close.md)— Закриває раніше відкрите з'єднання з базою даних
-   [mysqli::commit](mysqli.commit.md) \- Фіксує поточну транзакцію
-   [mysqli::$connect\_errno](mysqli.connect-errno.md)— Повертає код помилки останньої спроби з'єднання
-   [mysqli::$connect\_error](mysqli.connect-error.md)— Повертає опис останньої помилки підключення
-   [mysqli::\_\_construct](mysqli.construct.md)— Встановлює нове з'єднання із сервером MySQL
-   [mysqli::debug](mysqli.debug.md) \- Виконує процедури налагодження
-   [mysqli::dump\_debug\_info](mysqli.dump-debug-info.md) \- Журналування налагоджувальної інформації
-   [mysqli::$errno](mysqli.errno.md)— Повертає код помилки останнього виклику функції
-   [mysqli::$error\_list](mysqli.error-list.md)— Повертає перелік помилок виконання останньої запущеної команди
-   [mysqli::$error](mysqli.error.md)— Повертає рядок із описом останньої помилки
-   [mysqli::execute\_query](mysqli.execute-query.md)— Підготовляє, зв'язує параметри та виконує SQL-запит.
-   [mysqli::$field\_count](mysqli.field-count.md)— Повертає кількість стовпців, які торкнулися останнім запитом
-   [mysqli::get\_charset](mysqli.get-charset.md)— Повертає об'єкт, що описує кодування
-   [mysqli::$client\_info](mysqli.get-client-info.md)— Отримує інформацію про клієнта MySQL
-   [mysqli::$client\_version](mysqli.get-client-version.md)— Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli::get\_connection\_stats](mysqli.get-connection-stats.md)— Повертає статистику з'єднання із клієнтом
-   [mysqli::$host\_info](mysqli.get-host-info.md)— Повертає рядок, що містить тип використовуваної сполуки
-   [mysqli::$protocol\_version](mysqli.get-proto-info.md)— Повертає версію протоколу, що використовується MySQL
-   [mysqli::$server\_info](mysqli.get-server-info.md)— Повертає версію сервера MySQL
-   [mysqli::$server\_version](mysqli.get-server-version.md)— Повертає версію сервера MySQL, представлену у вигляді integer
-   [mysqli::get\_warnings](mysqli.get-warnings.md)— Отримує результат SHOW WARNINGS
-   [mysqli::$info](mysqli.info.md)— Витягує інформацію про останній запит
-   [mysqli::init](mysqli.init.md)— Ініціалізує MySQLi та повертає об'єкт для використання у функції mysqli\_real\_connect()
-   [mysqli::$insert\_id](mysqli.insert-id.md)— Повертає значення, створене для стовпця AUTO\_INCREMENT останнім запитом
-   [mysqli::kill](mysqli.kill.md)— Запит для сервера завершити виконання процесу MySQL
-   [mysqli::more\_results](mysqli.more-results.md)— Перевірка, чи є ще результати у мультизапиті
-   [mysqli::multi\_query](mysqli.multi-query.md)— Виконує один або кілька запитів до бази даних
-   [mysqli::next\_result](mysqli.next-result.md)— Підготовка наступного результуючого набору з multi\_query
-   [mysqli::options](mysqli.options.md)— Встановлення налаштувань
-   [mysqli::ping](mysqli.ping.md)— Перевіряє працездатність з'єднання або намагається перепідключитися, якщо з'єднання розірвано
-   [mysqli::poll](mysqli.poll.md) \- Опитування підключень
-   [mysqli::prepare](mysqli.prepare.md) \- Підготовляє SQL вираз до виконання
-   [mysqli::query](mysqli.query.md)— Виконує запит до бази даних
-   [mysqli::real\_connect](mysqli.real-connect.md)— Встановлює з'єднання із сервером mysql
-   [mysqli::real\_escape\_string](mysqli.real-escape-string.md)— Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
-   [mysqli::real\_query](mysqli.real-query.md) \- Виконання SQL запиту
-   [mysqli::reap\_async\_query](mysqli.reap-async-query.md)— Отримання результату асинхронного запиту
-   [mysqli::refresh](mysqli.refresh.md) \- Оновлення
-   [mysqli::release\_savepoint](mysqli.release-savepoint.md)— Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції.
-   [mysqli::rollback](mysqli.rollback.md) \- Відкат поточної транзакції
-   [mysqli::savepoint](mysqli.savepoint.md)— Встановіть іменовану точку збереження транзакції
-   [mysqli::select\_db](mysqli.select-db.md)— Встановлює базу даних для запитів, що виконуються.
-   [mysqli::set\_charset](mysqli.set-charset.md)— Задає набір символів
-   [mysqli::$sqlstate](mysqli.sqlstate.md)— Повертає код стану SQLSTATE останньої операції MySQL операції
-   [mysqli::ssl\_set](mysqli.ssl-set.md)— Використовується для встановлення безпечних з'єднань за допомогою SSL
-   [mysqli::stat](mysqli.stat.md) \- Отримання інформації про поточний стан системи
-   [mysqli::stmt\_init](mysqli.stmt-init.md)— Ініціалізує запит та повертає об'єкт для використання у mysqli\_stmt\_prepare
-   [mysqli::store\_result](mysqli.store-result.md)— передає на клієнта результуючий набір останнього запиту
-   [mysqli::$thread\_id](mysqli.thread-id.md)— Повертає ID процесу поточного підключення
-   [mysqli::thread\_safe](mysqli.thread-safe.md)— Показує, чи безпечна робота із процесами
-   [mysqli::use\_result](mysqli.use-result.md)— Готує результуючий набір на сервері для використання
-   [mysqli::$warning\_count](mysqli.warning-count.md)— Повертає кількість попереджень із останнього запиту заданого підключення
