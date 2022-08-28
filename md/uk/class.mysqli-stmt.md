The mysqlistmt class

-   [« mysqli::$warning\_count](mysqli.warning-count.html)
    
-   [mysqli\_stmt::$affected\_rows »](mysqli-stmt.affected-rows.html)
    
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

-   [mysqli\_stmt::$affected\_rows](mysqli-stmt.affected-rows.html) — Повертає загальну кількість рядків, змінених, віддалених, вставлених чи зіставлених останнім виконаним виразом
-   [mysqli\_stmt::attr\_get](mysqli-stmt.attr-get.html) — Отримує поточне значення атрибуту запиту
-   [mysqli\_stmt::attr\_set](mysqli-stmt.attr-set.html) — Змінює поведінку підготовленого запиту
-   [mysqli\_stmt::bind\_param](mysqli-stmt.bind-param.html) — Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt::bind\_result](mysqli-stmt.bind-result.html) — Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqli\_stmt::close](mysqli-stmt.close.html) - Закриває підготовлений запит
-   [mysqli\_stmt::\_\_construct](mysqli-stmt.construct.html) - Конструктор для об'єкту mysqlistmt
-   [mysqli\_stmt::data\_seek](mysqli-stmt.data-seek.html) — Перехід до заданого рядка в результуючому наборі
-   [mysqli\_stmt::$errno](mysqli-stmt.errno.html) — Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt::$error\_list](mysqli-stmt.error-list.html) — Повертає перелік помилок виконання останнього запиту
-   [mysqli\_stmt::$error](mysqli-stmt.error.html) — Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqli\_stmt::execute](mysqli-stmt.execute.html) - Виконує підготовлене твердження
-   [mysqli\_stmt::fetch](mysqli-stmt.fetch.html) — пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_stmt::$field\_count](mysqli-stmt.field-count.html) — Повертає кількість стовпців у заданому виразі
-   [mysqli\_stmt::free\_result](mysqli-stmt.free-result.html) — Звільняє пам'ять від результату запиту, вказаного дескриптором
-   [mysqli\_stmt::get\_result](mysqli-stmt.get-result.html) — Отримує результат із підготовленого запиту у вигляді об'єкту mysqliresult
-   [mysqli\_stmt::get\_warnings](mysqli-stmt.get-warnings.html) — Отримує результат від SHOW WARNINGS
-   [mysqli\_stmt::$insert\_id](mysqli-stmt.insert-id.html) — Отримує ID, згенероване попередньою операцією INSERT
-   [mysqli\_stmt::more\_results](mysqli-stmt.more-results.html) — Перевіряє, чи є ще набори рядків через мультизапит.
-   [mysqli\_stmt::next\_result](mysqli-stmt.next-result.html) — Читає наступний набір рядків із мультизапиту
-   [mysqli\_stmt::$num\_rows](mysqli-stmt.num-rows.html) — Повертає кількість рядків, отриманих із сервера
-   [mysqli\_stmt::$param\_count](mysqli-stmt.param-count.html) — Повертає кількість параметрів у запиті
-   [mysqli\_stmt::prepare](mysqli-stmt.prepare.html) — готує затвердження SQL до виконання
-   [mysqli\_stmt::reset](mysqli-stmt.reset.html) — скидає результати виконання підготовленого запиту
-   [mysqli\_stmt::result\_metadata](mysqli-stmt.result-metadata.html) — Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqli\_stmt::send\_long\_data](mysqli-stmt.send-long-data.html) — Надсилання даних блоками
-   [mysqli\_stmt::$sqlstate](mysqli-stmt.sqlstate.html) — Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
-   [mysqli\_stmt::store\_result](mysqli-stmt.store-result.html) — Зберігає набір результатів у внутрішньому буфері