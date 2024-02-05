---
navigation:
  - mysqli-stmt.store-result.md: '« mysqli\_stmt::store\_result'
  - mysqli-result.construct.md: 'mysqli\_result::\_\_construct »'
  - index.md: PHP Manual
  - book.mysqli.md: MySQLi
title: Клас mysqli\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас mysqli\_result

(PHP 5, PHP 7, PHP 8)

## Вступ

Надає результуючий набір, отриманий із запиту до бази даних.

## Огляд класів

```classsynopsis

    
     class mysqli_result
    

    
     implements
      IteratorAggregate {

    /* Свойства */
    
     public
     readonly
     int
      $current_field;

    public
     readonly
     int
      $field_count;

    public
     readonly
     ?array
      $lengths;

    public
     readonly
     int|string
      $num_rows;

    public
     int
      $type;


    /* Методы */
    
   public __construct(mysqli $mysql, int $result_mode = MYSQLI_STORE_RESULT)

    public data_seek(int $offset): bool
public fetch_all(int $mode = MYSQLI_NUM): array
public fetch_array(int $mode = MYSQLI_BOTH): array|null|false
public fetch_assoc(): array|null|false
public fetch_column(int $column = 0): null|int|float|string|false
public fetch_field_direct(int $index): object|false
public fetch_field(): object|false
public fetch_fields(): array
public fetch_object(string $class = "stdClass", array $constructor_args = []): object|null|false
public fetch_row(): array|null|false
public field_seek(int $index): bool
public free(): void
public close(): void
public free_result(): void
public getIterator(): Iterator

   }
```

## Властивості

type

Зберігає буферизований чи небуферизований результат як цілого числа (int) (\*\*`MYSQLI_STORE_RESULT`** або **`MYSQLI_USE_RESULT`\*\*соответственно).

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**mysqli\_result** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). . Раніше замість нього було реалізовано інтерфейс [Traversable](class.traversable.md) |

## Зміст

-   [mysqli\_result::\_\_construct](mysqli-result.construct.md) \- Конструктор об'єкта mysqli\_result
-   [mysqli\_result::$current\_field](mysqli-result.current-field.md)— Отримує зміщення вказівника щодо поточного поля
-   [mysqli\_result::data\_seek](mysqli-result.data-seek.md)— Переміщує покажчик результату на вибраний рядок
-   [mysqli\_result::fetch\_all](mysqli-result.fetch-all.md) \- Вибирає всі рядки з результуючого набору і поміщає їх в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_result::fetch\_array](mysqli-result.fetch-array.md)— Вибирає наступний рядок із набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_result::fetch\_assoc](mysqli-result.fetch-assoc.md)— Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_result::fetch\_column](mysqli-result.fetch-column.md)— Отримує один стовпець із наступного рядка набору результатів
-   [mysqli\_result::fetch\_field\_direct](mysqli-result.fetch-field-direct.md)— Отримання метаданих конкретного поля
-   [mysqli\_result::fetch\_field](mysqli-result.fetch-field.md)— Повертає наступне поле результуючого набору
-   [mysqli\_result::fetch\_fields](mysqli-result.fetch-fields.md)— Повертає масив об'єктів, що становлять поля результуючого набору
-   [mysqli\_result::fetch\_object](mysqli-result.fetch-object.md)— Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_result::fetch\_row](mysqli-result.fetch-row.md)— Вибирає наступний рядок із набору результатів та поміщає його у звичайний масив
-   [mysqli\_result::$field\_count](mysqli-result.field-count.md)— Отримує кількість полів у наборі результатів
-   [mysqli\_result::field\_seek](mysqli-result.field-seek.md)— Встановити покажчик поля на певне усунення
-   [mysqli\_result::free](mysqli-result.free.md) \- Звільняє пам'ять, зайняту результатами запиту
-   [mysqli\_result::getIterator](mysqli-result.getiterator.md) \- Витягує зовнішній ітератор
-   [mysqli\_result::$lengths](mysqli-result.lengths.md)— Повертає довжини полів поточного рядка результуючого набору
-   [mysqli\_result::$num\_rows](mysqli-result.num-rows.md)— Отримує кількість рядків у наборі результатів
