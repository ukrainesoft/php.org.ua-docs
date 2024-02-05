---
navigation:
  - mysqli.warning-count.md: '« mysqli::$warning\_count'
  - mysqli-stmt.affected-rows.md: 'mysqli\_stmt::$affected\_rows »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: The mysqli\_stmt class
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# The mysqli\_stmt class

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
public close(): true
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

id

Зберігає ідентифікатор оператора.

## Зміст

-   [mysqli\_stmt::$affected\_rows](mysqli-stmt.affected-rows.md)— Повертає загальну кількість рядків, змінених, віддалених, вставлених чи зіставлених останнім виконаним виразом
-   [mysqli\_stmt::attr\_get](mysqli-stmt.attr-get.md)— Отримує поточне значення атрибуту запиту
-   [mysqli\_stmt::attr\_set](mysqli-stmt.attr-set.md)— Змінює поведінку підготовленого запиту
-   [mysqli\_stmt::bind\_param](mysqli-stmt.bind-param.md)— Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt::bind\_result](mysqli-stmt.bind-result.md)— Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqli\_stmt::close](mysqli-stmt.close.md) \- Закриває підготовлений запит
-   [mysqli\_stmt::\_\_construct](mysqli-stmt.construct.md) \- Конструктор для об'єкту mysqli\_stmt
-   [mysqli\_stmt::data\_seek](mysqli-stmt.data-seek.md)— Коригує покажчик результату на довільний рядок у буферизованому результаті
-   [mysqli\_stmt::$errno](mysqli-stmt.errno.md)— Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt::$error\_list](mysqli-stmt.error-list.md)— Повертає перелік помилок виконання останнього запиту
-   [mysqli\_stmt::$error](mysqli-stmt.error.md)— Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqli\_stmt::execute](mysqli-stmt.execute.md) \- Виконує підготовлене твердження
-   [mysqli\_stmt::fetch](mysqli-stmt.fetch.md)— пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_stmt::$field\_count](mysqli-stmt.field-count.md)— Повертає кількість стовпців у заданому виразі
-   [mysqli\_stmt::free\_result](mysqli-stmt.free-result.md)— Звільняє пам'ять від результату запиту, вказаного дескриптором
-   [mysqli\_stmt::get\_result](mysqli-stmt.get-result.md)— Отримує результат із підготовленого запиту у вигляді об'єкту mysqli\_result
-   [mysqli\_stmt::get\_warnings](mysqli-stmt.get-warnings.md)— Отримує результат від SHOW WARNINGS
-   [mysqli\_stmt::$insert\_id](mysqli-stmt.insert-id.md)— Отримує ID, згенероване попередньою операцією INSERT
-   [mysqli\_stmt::more\_results](mysqli-stmt.more-results.md)— Перевіряє, чи є ще набори рядків через мультизапит.
-   [mysqli\_stmt::next\_result](mysqli-stmt.next-result.md)— Читає наступний набір рядків із мультизапиту
-   [mysqli\_stmt::$num\_rows](mysqli-stmt.num-rows.md)— Повертає кількість рядків, отриманих із сервера
-   [mysqli\_stmt::$param\_count](mysqli-stmt.param-count.md)— Повертає кількість параметрів у запиті
-   [mysqli\_stmt::prepare](mysqli-stmt.prepare.md)— готує затвердження SQL до виконання
-   [mysqli\_stmt::reset](mysqli-stmt.reset.md)— скидає результати виконання підготовленого запиту
-   [mysqli\_stmt::result\_metadata](mysqli-stmt.result-metadata.md)— Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqli\_stmt::send\_long\_data](mysqli-stmt.send-long-data.md)— Надсилання даних блоками
-   [mysqli\_stmt::$sqlstate](mysqli-stmt.sqlstate.md)— Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
-   [mysqli\_stmt::store\_result](mysqli-stmt.store-result.md)— Зберігає набір результатів у внутрішньому буфері
