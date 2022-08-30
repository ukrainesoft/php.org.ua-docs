The mysqlistmt class

-   [« mysqli::$warningcount](mysqli.warning-count.html)
    
-   [mysqlistmt::$affectedrows »](mysqli-stmt.affected-rows.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   The mysqlistmt class
    

# The mysqlistmt class

(PHP 5, PHP 7, PHP 8)

## Вступ

Представляє підготовлений вираз.

## Огляд класів

```classsynopsis

     
    

    
     
      class mysqli_stmt
     
     {

    /* Свойства */
    
     public
     readonly
     int|string
      $affected_rows;

    public
     readonly
     int|string
      $insert_id;

    public
     readonly
     int|string
      $num_rows;

    public
     readonly
     int
      $param_count;

    public
     readonly
     int
      $field_count;

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
     string
      $sqlstate;

    public
     int
      $id;


    /* Методы */
    
   public __construct(mysqli $mysql, ?string $query = null)

    public attr_get(int $attribute): int
public attr_set(int $attribute, int $value): bool
public bind_param(string $types, mixed &$var, mixed &...$vars): bool
public bind_result(mixed &$var, mixed &...$vars): bool
public close(): bool
public data_seek(int $offset): void
public execute(?array $params = null): bool
public fetch(): ?bool
public free_result(): void
public get_result(): mysqli_result|false
public get_warnings(): mysqli_warning|false
public more_results(): bool
public next_result(): bool
public num_rows(): int|string
public prepare(string $query): bool
public reset(): bool
public result_metadata(): mysqli_result|false
public send_long_data(int $param_num, string $data): bool
public store_result(): bool

   }
```

## Властивості

ід

Зберігає ідентифікатор оператора.

## Зміст

-   [mysqlistmt::$affectedrows](mysqli-stmt.affected-rows.html) — Повертає загальну кількість рядків, змінених, віддалених, вставлених чи зіставлених останнім виконаним виразом
-   [mysqlistmt::attrget](mysqli-stmt.attr-get.html) — Отримує поточне значення атрибуту запиту
-   [mysqlistmt::attrset](mysqli-stmt.attr-set.html) — Змінює поведінку підготовленого запиту
-   [mysqlistmt::bindparam](mysqli-stmt.bind-param.html) — Прив'язка змінних до параметрів запиту, що готується.
-   [mysqlistmt::bindresult](mysqli-stmt.bind-result.html) — Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqlistmt::close](mysqli-stmt.close.html) - Закриває підготовлений запит
-   [mysqlistmt::construct](mysqli-stmt.construct.html) - Конструктор для об'єкту mysqlistmt
-   [mysqlistmt::dataseek](mysqli-stmt.data-seek.html) — Перехід до заданого рядка в результуючому наборі
-   [mysqlistmt::$errno](mysqli-stmt.errno.html) — Повертає код помилки виконання останнього запиту
-   [mysqlistmt::$errorlist](mysqli-stmt.error-list.html) — Повертає перелік помилок виконання останнього запиту
-   [mysqlistmt::$error](mysqli-stmt.error.html) — Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqlistmt::execute](mysqli-stmt.execute.html) - Виконує підготовлене твердження
-   [mysqlistmt::fetch](mysqli-stmt.fetch.html) — пов'язує результати підготовленого виразу зі змінними
-   [mysqlistmt::$fieldcount](mysqli-stmt.field-count.html) — Повертає кількість стовпців у заданому виразі
-   [mysqlistmt::freeresult](mysqli-stmt.free-result.html) — Звільняє пам'ять від результату запиту, вказаного дескриптором
-   [mysqlistmt::getresult](mysqli-stmt.get-result.html) — Отримує результат із підготовленого запиту у вигляді об'єкту mysqliresult
-   [mysqlistmt::getwarnings](mysqli-stmt.get-warnings.html) — Отримує результат від SHOW WARNINGS
-   [mysqlistmt::$insertід](mysqli-stmt.insert-id.html) — Отримує ID, згенероване попередньою операцією INSERT
-   [mysqlistmt::moreresults](mysqli-stmt.more-results.html) — Перевіряє, чи є ще набори рядків через мультизапит.
-   [mysqlistmt::nextresult](mysqli-stmt.next-result.html) — Читає наступний набір рядків із мультизапиту
-   [mysqlistmt::$numrows](mysqli-stmt.num-rows.html) — Повертає кількість рядків, отриманих із сервера
-   [mysqlistmt::$paramcount](mysqli-stmt.param-count.html) — Повертає кількість параметрів у запиті
-   [mysqlistmt::prepare](mysqli-stmt.prepare.html) — готує затвердження SQL до виконання
-   [mysqlistmt::reset](mysqli-stmt.reset.html) — скидає результати виконання підготовленого запиту
-   [mysqlistmt::resultmetadata](mysqli-stmt.result-metadata.html) — Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqlistmt::sendlongdata](mysqli-stmt.send-long-data.html) — Надсилання даних блоками
-   [mysqlistmt::$sqlstate](mysqli-stmt.sqlstate.html) — Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
-   [mysqlistmt::storeresult](mysqli-stmt.store-result.html) — Зберігає набір результатів у внутрішньому буфері