Клас mysqliresult

-   [« mysqli\_stmt::store\_result](mysqli-stmt.store-result.html)
    
-   [mysqli\_result::\_\_construct »](mysqli-result.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MySQLi](book.mysqli.html)
    
-   Клас mysqliresult
    

# Клас mysqliresult

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

Зберігає буферизований чи небуферизований результат як цілого числа (int) (**`MYSQLI_STORE_RESULT`** або **`MYSQLI_USE_RESULT`** відповідно).

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **mysqliresult** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Раніше замість нього було реалізовано інтерфейс [Traversable](class.traversable.html) |

## Зміст

-   [mysqli\_result::\_\_construct](mysqli-result.construct.html) - Конструктор об'єкта mysqliresult
-   [mysqli\_result::$current\_field](mysqli-result.current-field.html) — Отримує зміщення вказівника щодо поточного поля
-   [mysqli\_result::data\_seek](mysqli-result.data-seek.html) — Переміщує покажчик результату на вибраний рядок
-   [mysqli\_result::fetch\_all](mysqli-result.fetch-all.html) - Вибирає всі рядки з результуючого набору і поміщає їх в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_result::fetch\_array](mysqli-result.fetch-array.html) — Вибирає наступний рядок із набору результатів і поміщає його в асоціативний масив, звичайний масив або в обидва
-   [mysqli\_result::fetch\_assoc](mysqli-result.fetch-assoc.html) — Вибирає наступний рядок із набору результатів та поміщає його в асоціативний масив
-   [mysqli\_result::fetch\_column](mysqli-result.fetch-column.html) — Отримує один стовпець із наступного рядка набору результатів
-   [mysqli\_result::fetch\_field\_direct](mysqli-result.fetch-field-direct.html) — Отримання метаданих конкретного поля
-   [mysqli\_result::fetch\_field](mysqli-result.fetch-field.html) — Повертає наступне поле результуючого набору
-   [mysqli\_result::fetch\_fields](mysqli-result.fetch-fields.html) — Повертає масив об'єктів, що становлять поля результуючого набору
-   [mysqli\_result::fetch\_object](mysqli-result.fetch-object.html) — Вибирає наступний рядок із набору результатів у вигляді об'єкта
-   [mysqli\_result::fetch\_row](mysqli-result.fetch-row.html) — Вибирає наступний рядок із набору результатів та поміщає його у звичайний масив
-   [mysqli\_result::$field\_count](mysqli-result.field-count.html) — Отримує кількість полів у наборі результатів
-   [mysqli\_result::field\_seek](mysqli-result.field-seek.html) — Встановити покажчик поля на певне усунення
-   [mysqli\_result::free](mysqli-result.free.html) - Звільняє пам'ять, зайняту результатами запиту
-   [mysqli\_result::getIterator](mysqli-result.getiterator.html) - Витягує зовнішній ітератор
-   [mysqli\_result::$lengths](mysqli-result.lengths.html) — Повертає довжини полів поточного рядка результуючого набору
-   [mysqli\_result::$num\_rows](mysqli-result.num-rows.html) — Отримує кількість рядків у наборі результатів