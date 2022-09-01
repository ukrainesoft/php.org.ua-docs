---
navigation:
  - mysqli.warning-count.html: '« mysqli::$warningcount'
  - mysqli-stmt.affected-rows.html: 'mysqlistmt::$affectedrows »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: The mysqlistmt class
---
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

-   [mysqlistmt::$affectedrows](mysqli-stmt.affected-rows.md) — Повертає загальну кількість рядків, змінених, віддалених, вставлених чи зіставлених останнім виконаним виразом
-   [mysqlistmt::attrget](mysqli-stmt.attr-get.md) — Отримує поточне значення атрибуту запиту
-   [mysqlistmt::attrset](mysqli-stmt.attr-set.md) — Змінює поведінку підготовленого запиту
-   [mysqlistmt::bindparam](mysqli-stmt.bind-param.md) — Прив'язка змінних до параметрів запиту, що готується.
-   [mysqlistmt::bindresult](mysqli-stmt.bind-result.md) — Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqlistmt::close](mysqli-stmt.close.md) - Закриває підготовлений запит
-   [mysqlistmt::construct](mysqli-stmt.construct.md) - Конструктор для об'єкту mysqlistmt
-   [mysqlistmt::dataseek](mysqli-stmt.data-seek.md) — Перехід до заданого рядка в результуючому наборі
-   [mysqlistmt::$errno](mysqli-stmt.errno.md) — Повертає код помилки виконання останнього запиту
-   [mysqlistmt::$errorlist](mysqli-stmt.error-list.md) — Повертає перелік помилок виконання останнього запиту
-   [mysqlistmt::$error](mysqli-stmt.error.md) — Повертає рядок із поясненням останньої помилки під час виконання запиту
-   [mysqlistmt::execute](mysqli-stmt.execute.md) - Виконує підготовлене твердження
-   [mysqlistmt::fetch](mysqli-stmt.fetch.md) — пов'язує результати підготовленого виразу зі змінними
-   [mysqlistmt::$fieldcount](mysqli-stmt.field-count.md) — Повертає кількість стовпців у заданому виразі
-   [mysqlistmt::freeresult](mysqli-stmt.free-result.md) — Звільняє пам'ять від результату запиту, вказаного дескриптором
-   [mysqlistmt::getresult](mysqli-stmt.get-result.md) — Отримує результат із підготовленого запиту у вигляді об'єкту mysqliresult
-   [mysqlistmt::getwarnings](mysqli-stmt.get-warnings.md) — Отримує результат від SHOW WARNINGS
-   [mysqlistmt::$insertід](mysqli-stmt.insert-id.md) — Отримує ID, згенероване попередньою операцією INSERT
-   [mysqlistmt::moreresults](mysqli-stmt.more-results.md) — Перевіряє, чи є ще набори рядків через мультизапит.
-   [mysqlistmt::nextresult](mysqli-stmt.next-result.md) — Читає наступний набір рядків із мультизапиту
-   [mysqlistmt::$numrows](mysqli-stmt.num-rows.md) — Повертає кількість рядків, отриманих із сервера
-   [mysqlistmt::$paramcount](mysqli-stmt.param-count.md) — Повертає кількість параметрів у запиті
-   [mysqlistmt::prepare](mysqli-stmt.prepare.md) — готує затвердження SQL до виконання
-   [mysqlistmt::reset](mysqli-stmt.reset.md) — скидає результати виконання підготовленого запиту
-   [mysqlistmt::resultmetadata](mysqli-stmt.result-metadata.md) — Повертає метадані результуючої таблиці запиту, що готується.
-   [mysqlistmt::sendlongdata](mysqli-stmt.send-long-data.md) — Надсилання даних блоками
-   [mysqlistmt::$sqlstate](mysqli-stmt.sqlstate.md) — Повертає код помилки SQLSTATE, викликаної під час виконання останньої операції над запитом
-   [mysqlistmt::storeresult](mysqli-stmt.store-result.md) — Зберігає набір результатів у внутрішньому буфері
